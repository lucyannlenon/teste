# Api Para digLivros
Url: https://api.suporte4.mutumnet.com.br/api/clientes/book/list

A formação da url deve conter como query string
```curl
 // Query string 
 start: int; // [opcional] utilizado em caso de necessidade de paginação para indicar o inicio dos registros
 limit: int; // [opcional] utilizado em caso de necessidade de paginação para indicar a quantidade de registros por pagina 
 token: string ; // chave para acesso aos registros 
```
## response in json
```json
{
  "rows": [
    {
      "nome": "string", `// string`
      "telefone": "string", `// string`
      "email": "string" `// string`
    }
  ],
  "total": 123 `// number`
}
```
## modelo do respone em typescript
```ts
    export interface Row {
        nome: string;
        telefone: string;
        email: string;
    }

    export interface Page {
        rows: Row[];
        total: number;
    }
```
