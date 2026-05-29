use ecommerceClientesDB
switched to db ecommerceClientesDB
use('ecommerceClientesDB');

db.clientes.drop();

const productos = [
  "Laptop", "Mouse", "Teclado", "Monitor", "Impresora",
  "Tablet", "Celular", "Audifonos", "Smartwatch", "Camara",
  "Disco Duro", "Memoria USB", "Router", "Silla Gamer", "Microfono"
];

const ciudades = [
  "San Salvador", "Santa Tecla", "Soyapango", "Mejicanos", "Apopa",
  "Lima", "Bogotá", "Quito", "Cali", "Medellín"
];

const paginas = [
  "Inicio", "Productos", "Ofertas", "Carrito", "Perfil",
  "Favoritos", "Detalle Producto", "Historial", "Pagos", "Soporte"
];

let clientes = [];

for (let i = 1; i <= 5000; i++) {
  let direcciones = [];
  let favoritos = [];
  let metodosPago = [];
  let compras = [];
  let historial = [];

  // 3 direcciones
  for (let d = 1; d <= 3; d++) {
    direcciones.push({
      tipo: d === 1 ? "Casa" : d === 2 ? "Trabajo" : "Otro",
      ciudad: ciudades[(i + d) % ciudades.length],
      direccion: `Calle ${d}, Avenida ${i}, Casa #${i + d}`
    });
  }

  // 10 productos favoritos sin duplicados
  for (let f = 0; f < 10; f++) {
    favoritos.push(productos[(i + f) % productos.length]);
  }

  // 5 métodos de pago
  for (let p = 1; p <= 5; p++) {
    metodosPago.push({
      tipo: p % 2 === 0 ? "Tarjeta Debito" : "Tarjeta Credito",
      proveedor: p % 2 === 0 ? "Mastercard" : "Visa",
      ultimosDigitos: String(1000 + i + p).slice(-4)
    });
  }

  // 20 compras
  for (let c = 1; c <= 20; c++) {
    compras.push({
      compraId: c,
      producto: productos[(i + c) % productos.length],
      monto: ((i + c) % 500) + 50,
      fecha: new Date(2026, (c % 12), (c % 28) + 1)
    });
  }

  // 30 registros de navegación
  for (let n = 1; n <= 30; n++) {
    historial.push({
      pagina: paginas[n % paginas.length],
      productoVisto: productos[(i + n) % productos.length],
      fecha: new Date(2026, (n % 12), (n % 28) + 1)
    });
  }

  clientes.push({
    clienteId: i,
    nombre: `Cliente ${i}`,
    correo: `cliente${i}@correo.com`,
    telefono: `7000${String(i).padStart(4, "0")}`,
    direcciones: direcciones,
    productosFavoritos: favoritos,
    metodosPago: metodosPago,
    compras: compras,
    historialNavegacion: historial
  });
}

db.clientes.insertMany(clientes);

db.clientes.countDocuments();
5000
db.clientes.countDocuments()
5000
db.clientes.find({
  productosFavoritos: "Laptop"
})
{
  _id: ObjectId('6a19267d64cc3604f348d6a3'),
  clienteId: 6,
  nombre: 'Cliente 6',
  correo: 'cliente6@correo.com',
  telefono: '70000006',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Quito',
      direccion: 'Calle 1, Avenida 6, Casa #7'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Cali',
      direccion: 'Calle 2, Avenida 6, Casa #8'
    },
    {
      tipo: 'Otro',
      ciudad: 'Medellín',
      direccion: 'Calle 3, Avenida 6, Casa #9'
    }
  ],
  productosFavoritos: [
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a4'),
  clienteId: 7,
  nombre: 'Cliente 7',
  correo: 'cliente7@correo.com',
  telefono: '70000007',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Cali',
      direccion: 'Calle 1, Avenida 7, Casa #8'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Medellín',
      direccion: 'Calle 2, Avenida 7, Casa #9'
    },
    {
      tipo: 'Otro',
      ciudad: 'San Salvador',
      direccion: 'Calle 3, Avenida 7, Casa #10'
    }
  ],
  productosFavoritos: [
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a5'),
  clienteId: 8,
  nombre: 'Cliente 8',
  correo: 'cliente8@correo.com',
  telefono: '70000008',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Medellín',
      direccion: 'Calle 1, Avenida 8, Casa #9'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'San Salvador',
      direccion: 'Calle 2, Avenida 8, Casa #10'
    },
    {
      tipo: 'Otro',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 3, Avenida 8, Casa #11'
    }
  ],
  productosFavoritos: [
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a6'),
  clienteId: 9,
  nombre: 'Cliente 9',
  correo: 'cliente9@correo.com',
  telefono: '70000009',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'San Salvador',
      direccion: 'Calle 1, Avenida 9, Casa #10'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 2, Avenida 9, Casa #11'
    },
    {
      tipo: 'Otro',
      ciudad: 'Soyapango',
      direccion: 'Calle 3, Avenida 9, Casa #12'
    }
  ],
  productosFavoritos: [
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a7'),
  clienteId: 10,
  nombre: 'Cliente 10',
  correo: 'cliente10@correo.com',
  telefono: '70000010',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 1, Avenida 10, Casa #11'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Soyapango',
      direccion: 'Calle 2, Avenida 10, Casa #12'
    },
    {
      tipo: 'Otro',
      ciudad: 'Mejicanos',
      direccion: 'Calle 3, Avenida 10, Casa #13'
    }
  ],
  productosFavoritos: [
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a8'),
  clienteId: 11,
  nombre: 'Cliente 11',
  correo: 'cliente11@correo.com',
  telefono: '70000011',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Soyapango',
      direccion: 'Calle 1, Avenida 11, Casa #12'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Mejicanos',
      direccion: 'Calle 2, Avenida 11, Casa #13'
    },
    {
      tipo: 'Otro',
      ciudad: 'Apopa',
      direccion: 'Calle 3, Avenida 11, Casa #14'
    }
  ],
  productosFavoritos: [
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet'
  ],
  metodosPago: [
{
      ultimosDigitos: '1015'
    },
    {
      tipo: 'Tarjeta Debito',
      proveedor: 'Mastercard',
      ultimosDigitos: '1016'
    },
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1017'
    }
  ],
  compras: [
    {
      compraId: 1,
      producto: 'Silla Gamer',
      monto: 63,
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      compraId: 2,
      producto: 'Microfono',
      monto: 64,
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      compraId: 3,
      producto: 'Laptop',
      monto: 65,
      fecha: 2026-04-04T06:00:00.000Z
    },
    {
      compraId: 4,
      producto: 'Mouse',
      monto: 66,
      fecha: 2026-05-05T06:00:00.000Z
    },
    {
      compraId: 5,
      producto: 'Teclado',
      monto: 67,
      fecha: 2026-06-06T06:00:00.000Z
    },
    {
      compraId: 6,
      producto: 'Monitor',
      monto: 68,
      fecha: 2026-07-07T06:00:00.000Z
    },
    {
      compraId: 7,
      producto: 'Impresora',
      monto: 69,
      fecha: 2026-08-08T06:00:00.000Z
    },
    {
      compraId: 8,
      producto: 'Tablet',
      monto: 70,
      fecha: 2026-09-09T06:00:00.000Z
    },
    {
      compraId: 9,
      producto: 'Celular',
      monto: 71,
      fecha: 2026-10-10T06:00:00.000Z
    },
    {
      compraId: 10,
      producto: 'Audifonos',
      monto: 72,
{
      monto: 71,
      fecha: 2026-09-09T06:00:00.000Z
    },
    {
      compraId: 9,
      producto: 'Audifonos',
      monto: 72,
      fecha: 2026-10-10T06:00:00.000Z
    },
    {
      compraId: 10,
      producto: 'Smartwatch',
      monto: 73,
      fecha: 2026-11-11T06:00:00.000Z
    },
    {
      compraId: 11,
      producto: 'Camara',
      monto: 74,
      fecha: 2026-12-12T06:00:00.000Z
    },
    {
      compraId: 12,
      producto: 'Disco Duro',
      monto: 75,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Memoria USB',
      monto: 76,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Router',
      monto: 77,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Silla Gamer',
      monto: 78,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Microfono',
      monto: 79,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Laptop',
      monto: 80,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Mouse',
      monto: 81,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Teclado',
      monto: 82,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Monitor',
{
  _id: ObjectId('6a19267d64cc3604f348d6ab'),
  clienteId: 14,
  nombre: 'Cliente 14',
  correo: 'cliente14@correo.com',
  telefono: '70000014',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Lima',
      direccion: 'Calle 1, Avenida 14, Casa #15'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Bogotá',
      direccion: 'Calle 2, Avenida 14, Casa #16'
    },
    {
      tipo: 'Otro',
      ciudad: 'Quito',
      direccion: 'Calle 3, Avenida 14, Casa #17'
    }
  ],
  productosFavoritos: [
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6ac'),
  clienteId: 15,
  nombre: 'Cliente 15',
  correo: 'cliente15@correo.com',
  telefono: '70000015',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Bogotá',
      direccion: 'Calle 1, Avenida 15, Casa #16'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Quito',
      direccion: 'Calle 2, Avenida 15, Casa #17'
    },
    {
      tipo: 'Otro',
      ciudad: 'Cali',
      direccion: 'Calle 3, Avenida 15, Casa #18'
    }
  ],
  productosFavoritos: [
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6b2'),
  clienteId: 21,
  nombre: 'Cliente 21',
  correo: 'cliente21@correo.com',
  telefono: '70000021',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Soyapango',
      direccion: 'Calle 1, Avenida 21, Casa #22'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Mejicanos',
      direccion: 'Calle 2, Avenida 21, Casa #23'
    },
    {
      tipo: 'Otro',
      ciudad: 'Apopa',
      direccion: 'Calle 3, Avenida 21, Casa #24'
    }
  ],
  productosFavoritos: [
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6b3'),
  clienteId: 22,
  nombre: 'Cliente 22',
  correo: 'cliente22@correo.com',
  telefono: '70000022',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Mejicanos',
      direccion: 'Calle 1, Avenida 22, Casa #23'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Apopa',
      direccion: 'Calle 2, Avenida 22, Casa #24'
    },
    {
      tipo: 'Otro',
      ciudad: 'Lima',
      direccion: 'Calle 3, Avenida 22, Casa #25'
    }
  ],
  productosFavoritos: [
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse'
  ],
  metodosPago: [
{
      fecha: 2026-08-08T06:00:00.000Z
    },
    {
      compraId: 8,
      producto: 'Mouse',
      monto: 81,
      fecha: 2026-09-09T06:00:00.000Z
    },
    {
      compraId: 9,
      producto: 'Teclado',
      monto: 82,
      fecha: 2026-10-10T06:00:00.000Z
    },
    {
      compraId: 10,
      producto: 'Monitor',
      monto: 83,
      fecha: 2026-11-11T06:00:00.000Z
    },
    {
      compraId: 11,
      producto: 'Impresora',
      monto: 84,
      fecha: 2026-12-12T06:00:00.000Z
    },
    {
      compraId: 12,
      producto: 'Tablet',
      monto: 85,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Celular',
      monto: 86,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Audifonos',
      monto: 87,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Smartwatch',
      monto: 88,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Camara',
      monto: 89,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Disco Duro',
      monto: 90,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Memoria USB',
      monto: 91,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Router',
      monto: 92,
{
  _id: ObjectId('6a19267d64cc3604f348d6b5'),
  clienteId: 24,
  nombre: 'Cliente 24',
  correo: 'cliente24@correo.com',
  telefono: '70000024',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Lima',
      direccion: 'Calle 1, Avenida 24, Casa #25'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Bogotá',
      direccion: 'Calle 2, Avenida 24, Casa #26'
    },
    {
      tipo: 'Otro',
      ciudad: 'Quito',
      direccion: 'Calle 3, Avenida 24, Casa #27'
    }
  ],
  productosFavoritos: [
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor'
  ],
  metodosPago: [
{
      proveedor: 'Visa',
      ultimosDigitos: '1030'
    }
  ],
  compras: [
    {
      compraId: 1,
      producto: 'Memoria USB',
      monto: 76,
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      compraId: 2,
      producto: 'Router',
      monto: 77,
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      compraId: 3,
      producto: 'Silla Gamer',
      monto: 78,
      fecha: 2026-04-04T06:00:00.000Z
    },
    {
      compraId: 4,
      producto: 'Microfono',
      monto: 79,
      fecha: 2026-05-05T06:00:00.000Z
    },
    {
      compraId: 5,
      producto: 'Laptop',
      monto: 80,
      fecha: 2026-06-06T06:00:00.000Z
    },
    {
      compraId: 6,
      producto: 'Mouse',
      monto: 81,
      fecha: 2026-07-07T06:00:00.000Z
    },
    {
      compraId: 7,
      producto: 'Teclado',
      monto: 82,
      fecha: 2026-08-08T06:00:00.000Z
    },
    {
      compraId: 8,
      producto: 'Monitor',
      monto: 83,
      fecha: 2026-09-09T06:00:00.000Z
    },
    {
      compraId: 9,
      producto: 'Impresora',
      monto: 84,
      fecha: 2026-10-10T06:00:00.000Z
    },
    {
      compraId: 10,
      producto: 'Tablet',
      monto: 85,
      fecha: 2026-11-11T06:00:00.000Z
    },
    {
      compraId: 11,
      producto: 'Celular',
      monto: 86,
      fecha: 2026-12-12T06:00:00.000Z
    },
    {
{
  _id: ObjectId('6a19267d64cc3604f348d6b7'),
  clienteId: 26,
  nombre: 'Cliente 26',
  correo: 'cliente26@correo.com',
  telefono: '70000026',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Quito',
      direccion: 'Calle 1, Avenida 26, Casa #27'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Cali',
      direccion: 'Calle 2, Avenida 26, Casa #28'
    },
    {
      tipo: 'Otro',
      ciudad: 'Medellín',
      direccion: 'Calle 3, Avenida 26, Casa #29'
    }
  ],
  productosFavoritos: [
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6b8'),
  clienteId: 27,
  nombre: 'Cliente 27',
  correo: 'cliente27@correo.com',
  telefono: '70000027',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Cali',
      direccion: 'Calle 1, Avenida 27, Casa #28'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Medellín',
      direccion: 'Calle 2, Avenida 27, Casa #29'
    },
    {
      tipo: 'Otro',
      ciudad: 'San Salvador',
      direccion: 'Calle 3, Avenida 27, Casa #30'
    }
  ],
  productosFavoritos: [
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6b9'),
  clienteId: 28,
  nombre: 'Cliente 28',
  correo: 'cliente28@correo.com',
  telefono: '70000028',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Medellín',
      direccion: 'Calle 1, Avenida 28, Casa #29'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'San Salvador',
      direccion: 'Calle 2, Avenida 28, Casa #30'
    },
    {
      tipo: 'Otro',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 3, Avenida 28, Casa #31'
    }
  ],
  productosFavoritos: [
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6ba'),
  clienteId: 29,
  nombre: 'Cliente 29',
  correo: 'cliente29@correo.com',
  telefono: '70000029',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'San Salvador',
      direccion: 'Calle 1, Avenida 29, Casa #30'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 2, Avenida 29, Casa #31'
    },
    {
      tipo: 'Otro',
      ciudad: 'Soyapango',
      direccion: 'Calle 3, Avenida 29, Casa #32'
    }
  ],
  productosFavoritos: [
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch'
  ],
  metodosPago: [
{
      fecha: 2026-12-12T06:00:00.000Z
    },
    {
      compraId: 12,
      producto: 'Router',
      monto: 92,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Silla Gamer',
      monto: 93,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Microfono',
      monto: 94,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Laptop',
      monto: 95,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Mouse',
      monto: 96,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Teclado',
      monto: 97,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Monitor',
      monto: 98,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Impresora',
      monto: 99,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Tablet',
      monto: 100,
      fecha: 2026-09-21T06:00:00.000Z
    }
  ],
  historialNavegacion: [
    {
      pagina: 'Productos',
      productoVisto: 'Mouse',
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      pagina: 'Ofertas',
      productoVisto: 'Teclado',
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      pagina: 'Carrito',
Type "it" for more
db.clientes.find({
  productosFavoritos: "Laptop"
}).limit(5)
{
  _id: ObjectId('6a19267d64cc3604f348d6a3'),
  clienteId: 6,
  nombre: 'Cliente 6',
  correo: 'cliente6@correo.com',
  telefono: '70000006',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Quito',
      direccion: 'Calle 1, Avenida 6, Casa #7'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Cali',
      direccion: 'Calle 2, Avenida 6, Casa #8'
    },
    {
      tipo: 'Otro',
      ciudad: 'Medellín',
      direccion: 'Calle 3, Avenida 6, Casa #9'
    }
  ],
  productosFavoritos: [
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a4'),
  clienteId: 7,
  nombre: 'Cliente 7',
  correo: 'cliente7@correo.com',
  telefono: '70000007',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Cali',
      direccion: 'Calle 1, Avenida 7, Casa #8'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Medellín',
      direccion: 'Calle 2, Avenida 7, Casa #9'
    },
    {
      tipo: 'Otro',
      ciudad: 'San Salvador',
      direccion: 'Calle 3, Avenida 7, Casa #10'
    }
  ],
  productosFavoritos: [
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d6a5'),
  clienteId: 8,
  nombre: 'Cliente 8',
  correo: 'cliente8@correo.com',
  telefono: '70000008',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Medellín',
      direccion: 'Calle 1, Avenida 8, Casa #9'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'San Salvador',
      direccion: 'Calle 2, Avenida 8, Casa #10'
    },
    {
      tipo: 'Otro',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 3, Avenida 8, Casa #11'
    }
  ],
  productosFavoritos: [
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado'
  ],
  metodosPago: [
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1009'
    },
    {
      tipo: 'Tarjeta Debito',
      proveedor: 'Mastercard',
      ultimosDigitos: '1010'
    },
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1011'
    },
    {
      tipo: 'Tarjeta Debito',
      proveedor: 'Mastercard',
      ultimosDigitos: '1012'
    },
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1013'
    }
  ],
  compras: [
    {
      compraId: 1,
      producto: 'Camara',
{
  _id: ObjectId('6a19267d64cc3604f348d6a6'),
  clienteId: 9,
  nombre: 'Cliente 9',
  correo: 'cliente9@correo.com',
  telefono: '70000009',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'San Salvador',
      direccion: 'Calle 1, Avenida 9, Casa #10'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 2, Avenida 9, Casa #11'
    },
    {
      tipo: 'Otro',
      ciudad: 'Soyapango',
      direccion: 'Calle 3, Avenida 9, Casa #12'
    }
  ],
  productosFavoritos: [
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor'
  ],
  metodosPago: [
{
    },
    {
      compraId: 12,
      producto: 'Audifonos',
      monto: 72,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Smartwatch',
      monto: 73,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Camara',
      monto: 74,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Disco Duro',
      monto: 75,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Memoria USB',
      monto: 76,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Router',
      monto: 77,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Silla Gamer',
      monto: 78,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Microfono',
      monto: 79,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Laptop',
      monto: 80,
      fecha: 2026-09-21T06:00:00.000Z
    }
  ],
  historialNavegacion: [
    {
      pagina: 'Productos',
      productoVisto: 'Memoria USB',
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      pagina: 'Ofertas',
      productoVisto: 'Router',
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      pagina: 'Carrito',
db.clientes.find({
  "compras.monto": { $gt: 300 }
})
{
      monto: 292,
      fecha: 2026-12-12T06:00:00.000Z
    },
    {
      compraId: 12,
      producto: 'Monitor',
      monto: 293,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Impresora',
      monto: 294,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Tablet',
      monto: 295,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Celular',
      monto: 296,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Audifonos',
      monto: 297,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Smartwatch',
      monto: 298,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Camara',
      monto: 299,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Disco Duro',
      monto: 300,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Memoria USB',
      monto: 301,
      fecha: 2026-09-21T06:00:00.000Z
    }
  ],
  historialNavegacion: [
    {
      pagina: 'Productos',
      productoVisto: 'Audifonos',
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      pagina: 'Ofertas',
      productoVisto: 'Smartwatch',
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      pagina: 'Carrito',
{
  _id: ObjectId('6a19267d64cc3604f348d785'),
  clienteId: 232,
  nombre: 'Cliente 232',
  correo: 'cliente232@correo.com',
  telefono: '70000232',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Mejicanos',
      direccion: 'Calle 1, Avenida 232, Casa #233'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Apopa',
      direccion: 'Calle 2, Avenida 232, Casa #234'
    },
    {
      tipo: 'Otro',
      ciudad: 'Lima',
      direccion: 'Calle 3, Avenida 232, Casa #235'
    }
  ],
  productosFavoritos: [
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d786'),
  clienteId: 233,
  nombre: 'Cliente 233',
  correo: 'cliente233@correo.com',
  telefono: '70000233',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Apopa',
      direccion: 'Calle 1, Avenida 233, Casa #234'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Lima',
      direccion: 'Calle 2, Avenida 233, Casa #235'
    },
    {
      tipo: 'Otro',
      ciudad: 'Bogotá',
      direccion: 'Calle 3, Avenida 233, Casa #236'
    }
  ],
  productosFavoritos: [
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d787'),
  clienteId: 234,
  nombre: 'Cliente 234',
  correo: 'cliente234@correo.com',
  telefono: '70000234',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Lima',
      direccion: 'Calle 1, Avenida 234, Casa #235'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Bogotá',
      direccion: 'Calle 2, Avenida 234, Casa #236'
    },
    {
      tipo: 'Otro',
      ciudad: 'Quito',
      direccion: 'Calle 3, Avenida 234, Casa #237'
    }
  ],
  productosFavoritos: [
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d788'),
  clienteId: 235,
  nombre: 'Cliente 235',
  correo: 'cliente235@correo.com',
  telefono: '70000235',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Bogotá',
      direccion: 'Calle 1, Avenida 235, Casa #236'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Quito',
      direccion: 'Calle 2, Avenida 235, Casa #237'
    },
    {
      tipo: 'Otro',
      ciudad: 'Cali',
      direccion: 'Calle 3, Avenida 235, Casa #238'
    }
  ],
  productosFavoritos: [
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d789'),
  clienteId: 236,
  nombre: 'Cliente 236',
  correo: 'cliente236@correo.com',
  telefono: '70000236',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Quito',
      direccion: 'Calle 1, Avenida 236, Casa #237'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Cali',
      direccion: 'Calle 2, Avenida 236, Casa #238'
    },
    {
      tipo: 'Otro',
      ciudad: 'Medellín',
      direccion: 'Calle 3, Avenida 236, Casa #239'
    }
  ],
  productosFavoritos: [
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet'
  ],
  metodosPago: [
{
      direccion: 'Calle 3, Avenida 237, Casa #240'
    }
  ],
  productosFavoritos: [
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular'
  ],
  metodosPago: [
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1238'
    },
    {
      tipo: 'Tarjeta Debito',
      proveedor: 'Mastercard',
      ultimosDigitos: '1239'
    },
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1240'
    },
    {
      tipo: 'Tarjeta Debito',
      proveedor: 'Mastercard',
      ultimosDigitos: '1241'
    },
    {
      tipo: 'Tarjeta Credito',
      proveedor: 'Visa',
      ultimosDigitos: '1242'
    }
  ],
  compras: [
    {
      compraId: 1,
      producto: 'Silla Gamer',
      monto: 288,
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      compraId: 2,
      producto: 'Microfono',
      monto: 289,
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      compraId: 3,
      producto: 'Laptop',
      monto: 290,
      fecha: 2026-04-04T06:00:00.000Z
    },
    {
      compraId: 4,
      producto: 'Mouse',
      monto: 291,
      fecha: 2026-05-05T06:00:00.000Z
    },
    {
      compraId: 5,
      producto: 'Teclado',
      monto: 292,
      fecha: 2026-06-06T06:00:00.000Z
{
  _id: ObjectId('6a19267d64cc3604f348d78b'),
  clienteId: 238,
  nombre: 'Cliente 238',
  correo: 'cliente238@correo.com',
  telefono: '70000238',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Medellín',
      direccion: 'Calle 1, Avenida 238, Casa #239'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'San Salvador',
      direccion: 'Calle 2, Avenida 238, Casa #240'
    },
    {
      tipo: 'Otro',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 3, Avenida 238, Casa #241'
    }
  ],
  productosFavoritos: [
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d78c'),
  clienteId: 239,
  nombre: 'Cliente 239',
  correo: 'cliente239@correo.com',
  telefono: '70000239',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'San Salvador',
      direccion: 'Calle 1, Avenida 239, Casa #240'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 2, Avenida 239, Casa #241'
    },
    {
      tipo: 'Otro',
      ciudad: 'Soyapango',
      direccion: 'Calle 3, Avenida 239, Casa #242'
    }
  ],
  productosFavoritos: [
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d78d'),
  clienteId: 240,
  nombre: 'Cliente 240',
  correo: 'cliente240@correo.com',
  telefono: '70000240',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 1, Avenida 240, Casa #241'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Soyapango',
      direccion: 'Calle 2, Avenida 240, Casa #242'
    },
    {
      tipo: 'Otro',
      ciudad: 'Mejicanos',
      direccion: 'Calle 3, Avenida 240, Casa #243'
    }
  ],
  productosFavoritos: [
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara'
  ],
  metodosPago: [
{
      compraId: 15,
      producto: 'Mouse',
      monto: 306,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Teclado',
      monto: 307,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Monitor',
      monto: 308,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Impresora',
      monto: 309,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Tablet',
      monto: 310,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Celular',
      monto: 311,
      fecha: 2026-09-21T06:00:00.000Z
    }
  ],
  historialNavegacion: [
    {
      pagina: 'Productos',
      productoVisto: 'Teclado',
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      pagina: 'Ofertas',
      productoVisto: 'Monitor',
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      pagina: 'Carrito',
{
  _id: ObjectId('6a19267d64cc3604f348d78f'),
  clienteId: 242,
  nombre: 'Cliente 242',
  correo: 'cliente242@correo.com',
  telefono: '70000242',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Mejicanos',
      direccion: 'Calle 1, Avenida 242, Casa #243'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Apopa',
      direccion: 'Calle 2, Avenida 242, Casa #244'
    },
    {
      tipo: 'Otro',
      ciudad: 'Lima',
      direccion: 'Calle 3, Avenida 242, Casa #245'
    }
  ],
  productosFavoritos: [
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d790'),
  clienteId: 243,
  nombre: 'Cliente 243',
  correo: 'cliente243@correo.com',
  telefono: '70000243',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Apopa',
      direccion: 'Calle 1, Avenida 243, Casa #244'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Lima',
      direccion: 'Calle 2, Avenida 243, Casa #245'
    },
    {
      tipo: 'Otro',
      ciudad: 'Bogotá',
      direccion: 'Calle 3, Avenida 243, Casa #246'
    }
  ],
  productosFavoritos: [
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router'
  ],
  metodosPago: [
{
    },
    {
      compraId: 12,
      producto: 'Mouse',
      monto: 306,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Teclado',
      monto: 307,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Monitor',
      monto: 308,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Impresora',
      monto: 309,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Tablet',
      monto: 310,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Celular',
      monto: 311,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Audifonos',
      monto: 312,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Smartwatch',
      monto: 313,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Camara',
      monto: 314,
      fecha: 2026-09-21T06:00:00.000Z
    }
  ],
  historialNavegacion: [
    {
      pagina: 'Productos',
      productoVisto: 'Tablet',
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      pagina: 'Ofertas',
      productoVisto: 'Celular',
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      pagina: 'Carrito',
{
  _id: ObjectId('6a19267d64cc3604f348d792'),
  clienteId: 245,
  nombre: 'Cliente 245',
  correo: 'cliente245@correo.com',
  telefono: '70000245',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Bogotá',
      direccion: 'Calle 1, Avenida 245, Casa #246'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Quito',
      direccion: 'Calle 2, Avenida 245, Casa #247'
    },
    {
      tipo: 'Otro',
      ciudad: 'Cali',
      direccion: 'Calle 3, Avenida 245, Casa #248'
    }
  ],
  productosFavoritos: [
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono'
  ],
  metodosPago: [
{
    },
    {
      compraId: 6,
      producto: 'Router',
      monto: 302,
      fecha: 2026-07-07T06:00:00.000Z
    },
    {
      compraId: 7,
      producto: 'Silla Gamer',
      monto: 303,
      fecha: 2026-08-08T06:00:00.000Z
    },
    {
      compraId: 8,
      producto: 'Microfono',
      monto: 304,
      fecha: 2026-09-09T06:00:00.000Z
    },
    {
      compraId: 9,
      producto: 'Laptop',
      monto: 305,
      fecha: 2026-10-10T06:00:00.000Z
    },
    {
      compraId: 10,
      producto: 'Mouse',
      monto: 306,
      fecha: 2026-11-11T06:00:00.000Z
    },
    {
      compraId: 11,
      producto: 'Teclado',
      monto: 307,
      fecha: 2026-12-12T06:00:00.000Z
    },
    {
      compraId: 12,
      producto: 'Monitor',
      monto: 308,
      fecha: 2026-01-13T06:00:00.000Z
    },
    {
      compraId: 13,
      producto: 'Impresora',
      monto: 309,
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Tablet',
      monto: 310,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Celular',
      monto: 311,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Audifonos',
      monto: 312,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Smartwatch',
      monto: 313,
{
  _id: ObjectId('6a19267d64cc3604f348d794'),
  clienteId: 247,
  nombre: 'Cliente 247',
  correo: 'cliente247@correo.com',
  telefono: '70000247',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Cali',
      direccion: 'Calle 1, Avenida 247, Casa #248'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Medellín',
      direccion: 'Calle 2, Avenida 247, Casa #249'
    },
    {
      tipo: 'Otro',
      ciudad: 'San Salvador',
      direccion: 'Calle 3, Avenida 247, Casa #250'
    }
  ],
  productosFavoritos: [
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse'
  ],
  metodosPago: [
{
  _id: ObjectId('6a19267d64cc3604f348d795'),
  clienteId: 248,
  nombre: 'Cliente 248',
  correo: 'cliente248@correo.com',
  telefono: '70000248',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Medellín',
      direccion: 'Calle 1, Avenida 248, Casa #249'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'San Salvador',
      direccion: 'Calle 2, Avenida 248, Casa #250'
    },
    {
      tipo: 'Otro',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 3, Avenida 248, Casa #251'
    }
  ],
  productosFavoritos: [
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado'
  ],
  metodosPago: [
{
      fecha: 2026-02-14T06:00:00.000Z
    },
    {
      compraId: 14,
      producto: 'Smartwatch',
      monto: 313,
      fecha: 2026-03-15T06:00:00.000Z
    },
    {
      compraId: 15,
      producto: 'Camara',
      monto: 314,
      fecha: 2026-04-16T06:00:00.000Z
    },
    {
      compraId: 16,
      producto: 'Disco Duro',
      monto: 315,
      fecha: 2026-05-17T06:00:00.000Z
    },
    {
      compraId: 17,
      producto: 'Memoria USB',
      monto: 316,
      fecha: 2026-06-18T06:00:00.000Z
    },
    {
      compraId: 18,
      producto: 'Router',
      monto: 317,
      fecha: 2026-07-19T06:00:00.000Z
    },
    {
      compraId: 19,
      producto: 'Silla Gamer',
      monto: 318,
      fecha: 2026-08-20T06:00:00.000Z
    },
    {
      compraId: 20,
      producto: 'Microfono',
      monto: 319,
      fecha: 2026-09-21T06:00:00.000Z
    }
  ],
  historialNavegacion: [
    {
      pagina: 'Productos',
      productoVisto: 'Disco Duro',
      fecha: 2026-02-02T06:00:00.000Z
    },
    {
      pagina: 'Ofertas',
      productoVisto: 'Memoria USB',
      fecha: 2026-03-03T06:00:00.000Z
    },
    {
      pagina: 'Carrito',
{
  _id: ObjectId('6a19267d64cc3604f348d797'),
  clienteId: 250,
  nombre: 'Cliente 250',
  correo: 'cliente250@correo.com',
  telefono: '70000250',
  direcciones: [
    {
      tipo: 'Casa',
      ciudad: 'Santa Tecla',
      direccion: 'Calle 1, Avenida 250, Casa #251'
    },
    {
      tipo: 'Trabajo',
      ciudad: 'Soyapango',
      direccion: 'Calle 2, Avenida 250, Casa #252'
    },
    {
      tipo: 'Otro',
      ciudad: 'Mejicanos',
      direccion: 'Calle 3, Avenida 250, Casa #253'
    }
  ],
  productosFavoritos: [
    'Disco Duro',
    'Memoria USB',
    'Router',
    'Silla Gamer',
    'Microfono',
    'Laptop',
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora'
  ],
Type "it" for more
db.clientes.countDocuments({
  "compras.10": { $exists: true }
})
5000
db.clientes.updateOne(
  { clienteId: 1 },
  {
    $push: {
      productosFavoritos: "PlayStation 5"
    }
  }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.clientes.findOne(
  { clienteId: 1 },
  { nombre: 1, productosFavoritos: 1, _id: 0 }
)
{
  nombre: 'Cliente 1',
  productosFavoritos: [
    'Mouse',
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'PlayStation 5'
  ]
}
db.clientes.updateOne(
  { clienteId: 1 },
  {
    $pull: {
      productosFavoritos: "Mouse"
    }
  }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.clientes.findOne(
  { clienteId: 1 },
  { nombre: 1, productosFavoritos: 1, _id: 0 }
)
{
  nombre: 'Cliente 1',
  productosFavoritos: [
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'PlayStation 5'
  ]
}
db.clientes.updateOne(
  { clienteId: 1 },
  {
    $addToSet: {
      productosFavoritos: "Laptop"
    }
  }
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.clientes.findOne(
  { clienteId: 1 },
  { nombre: 1, productosFavoritos: 1, _id: 0 }
)
{
  nombre: 'Cliente 1',
  productosFavoritos: [
    'Teclado',
    'Monitor',
    'Impresora',
    'Tablet',
    'Celular',
    'Audifonos',
    'Smartwatch',
    'Camara',
    'Disco Duro',
    'PlayStation 5',
    'Laptop'
  ]
}
ecommerceClientesDB
db.clientes.updateOne(
  { clienteId: 1 },
  {
    $addToSet: {
      productosFavoritos: "Laptop"
    }
  }
)

