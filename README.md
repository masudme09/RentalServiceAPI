This project is developed as a backend API for a Manufacturing Equipment Rental Service company. 
Following services has been implemented:
- NewPlantHireRequest(plantName string, siteName string, supplierName string, requesterName string,
		startDate time.Time, endDate time.Time, totalHiringCost float64, status int64) (*domain.PlantHireRequest, error): Here Plant represent Manufacturing Equipment. So, to hire new equipment endpoint is: "/requests/new"
- GetPlantHireRequestById(plantRequestId int64)
- ModifyRequestBySiteEngineers(plantRequestId int64, plantName string, siteName string, supplierName string,
		requesterName string, startDate time.Time, endDate time.Time, totalHiringCost float64) error
- ModifyRequestByWorkEngineers(plantRequestId int64, plantName string, siteName string, supplierName string,
		requesterName string, startDate time.Time, endDate time.Time, totalHiringCost float64) error
- AcceptRequest(plantRequestId int64, regulator string, comment string) error
- RejectRequest(plantRequestId int64, regulator string, comment string) error
- GetCompleteOrders() ([]*domain.CompleteOrder, error)
- CancelPlantHireRequest(plantHireRequestId int64, requesterName string, comment string) error
- RequestExtension(plantHireRequestID int64, endTime time.Time) (*domain.PlantOrder, error)
- AcceptInvoice(invoiceId int64, requesterName string, comment string) (*domain.Invoice, error)
- RejectInvoice(invoiceId int64, requesterName string, comment string) (*domain.Invoice, error)
- GetPurchaseOrderByInvoiceId(invoiceId int64) (*domain.CompleteOrder, error)
- DeleteRequestsBySupplierName(supplierName string) ([]*domain.PlantHireRequest, error)
- GeneratePurchaseOrder(plantHireRequestId int64) (*domain.PlantOrder, error)
- CheckInvoice(invoice *domain.Invoice) error
- NewInvoice(invoice *domain.Invoice) (*domain.Invoice, error)
- GetInvoiceById(invoiceId int64) (*domain.Invoice, error)

	
	
	
	

	
	
	
	

	
	
	
	
