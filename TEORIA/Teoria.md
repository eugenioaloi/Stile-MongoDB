# INSERT DOCUMENT (Single insert)

db.nomeDb.insertOne({OBJ})

OBJ-> è il documento che si vuole inserire nella collezione

# INSERT MANY DOCUMENTS (Many X insert)

db.nomeDb.insertMany([
    {OBJ},
    {OBJ}
])

# FIND DOCUMENTS 

db.nomeDb.find({FILTER})

FILTER -> è il filtro per ricercare il documento sarà composto da "chiave":"valore"

# FIND NESTED DOCUMENTS

db.nomeDb.find({
    "DocumentoN.documentoN1"
})

DocumentoN.documentoN1 -> è la chiave che si trova ad un livello di alberatura del documento 

eg. {
        {
            Documento N:
                {
                    Documento N1:"valore 1",        Documento N2:"valore 2",
                }
        }
    }

# RETURN SPECIFIC FIELDS IN A QUERY FIND

db.nomeDb.find({FILTER},{CHIAVE:1})

FILTER -> è il filtro applicato alla query
CHIAVE:1 -> è la chiave che se assegnato 1 fa restituire solo quella chiave

# COUNT THE RECORDS WHIT SPECIFIC QUERY FILTER

db.nomeDb.find({FILTER}).count()

# SORT THE RECORDS WHIT SPECIFIC FILTER

db.nomeDb.find({FILTER}).sort({CHIAVE:1})

CHIAVE:1 -> è la chiave di ordinamento ASC
CHIAVE:1 -> è la chiave di ordinamento DESC

# RECORD WITH LOGICAL OPERATOR (great, less than etc)

db.nomeDb.find({CHIAVE:{$OPERATORE:"something"}})

$OPERATORE: 

$gt -> greater than
$lt -> less than
$or -> one filter or the other matches






