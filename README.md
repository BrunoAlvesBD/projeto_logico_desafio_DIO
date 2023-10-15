# projeto_logico_desafio_DIO
Entidades e Atributos:

Clients:

idClient (Chave Primária)
Fname
Minit
Lname
CPF (Chave Única)
Address
Type
Product:

idProduct (Chave Primária)
Pname
Classification_kids
Category
Avaliacao
Size
Payments:

idPayment (Chave Primária)
TypePayment
LimitAvailable
Orders:

idOrder (Chave Primária)
idOrderClient (Chave Estrangeira referenciando Clients)
OrderStatus
OrderDescription
SendValue
PaymentCash
idPayment (Chave Estrangeira referenciando Payments)
Delivery:

idDelivery (Chave Primária)
idOrder (Chave Estrangeira referenciando Orders)
Status
TrackingCode
ProductStorage:

idProdStorage (Chave Primária)
StorageLocation
Quantity
Supplier:

idSupplier (Chave Primária)
SocialName
CNPJ (Chave Única)
Contact
Seller:

idSeller (Chave Primária)
SocialName
AbstName
CNPJ (Chave Única)
CPF (Chave Única)
Location
Contact
Relacionamentos:

Clients (idClient) -> Orders (idOrderClient)
Orders (idPayment) -> Payments (idPayment)
Orders (idOrder) -> Delivery (idOrder)
Orders (idOrderClient) -> Clients (idClient)
ProductSeller (idPsProduct) -> Product (idProduct)
ProductSeller (idPseller) -> Seller (idSeller)
ProductOrder (idPOproduct) -> Product (idProduct)
ProductOrder (idPOorder) -> Orders (idOrder)
StorageLocation (idLproduct) -> Product (idProduct)
StorageLocation (idLstorage) -> ProductStorage (idProdStorage)
ProductSupplier (idPsProduct) -> Product (idProduct)
ProductSupplier (idPsSupplier) -> Supplier (idSupplier)
