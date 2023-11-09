# proyecto-final-progra


package gui;

import javax.swing.*;

import java.awt.*;

import java.awt.event.ActionEvent;

import java.awt.event.ActionListener;

class CafeteriaAppGUI extends JFrame implements ActionListener {
    private Cafeteria cafeteria;

    private JTextField productoNombreField;
    private JTextField productoPorcionesField;
    private JTextField productoPrecioField;

    private JTextField facturacionNITField;
    private JTextField facturacionDescripcionField;
    private JTextField facturacionCantidadField;
    private JTextField facturacionPrecioField;

    private JTextField sobresDeCafeField;
    private JTextField librasDeAzucarField;
    private JTextField litrosDeLecheField;

    private JTextField ordenCodigoField;
    private JTextField ordenVentaField;
    private JTextField ordenVendedorField;

    private JTextField empleadoNombreField;
    private JTextField empleadoPuestoField;
    private JTextField empleadoVentasField;

    public CafeteriaAppGUI(Cafeteria cafeteria) {
        this.cafeteria = cafeteria;
        initialize();
    }

    private void initialize() {
        setTitle("Cafetería App");
        setSize(600, 400);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(new BorderLayout());

        JTabbedPane tabbedPane = new JTabbedPane();

        // Paneles para diferentes funciones
        JPanel agregarProductoPanel = createAgregarProductoPanel();
        JPanel facturacionPanel = createFacturacionPanel();
        JPanel inventarioPanel = createInventarioPanel();
        JPanel informacionOrdenPanel = createInformacionOrdenPanel();
        JPanel empleadoDelMesPanel = createEmpleadoDelMesPanel();

        tabbedPane.addTab("Agregar Producto", agregarProductoPanel);
        tabbedPane.addTab("Facturación", facturacionPanel);
        tabbedPane.addTab("Inventario", inventarioPanel);
        tabbedPane.addTab("Información de la Orden", informacionOrdenPanel);
        tabbedPane.addTab("Empleado del Mes", empleadoDelMesPanel);

        add(tabbedPane);
    }

    private JPanel createAgregarProductoPanel() {
    	 JPanel panel = new JPanel();
    	    panel.setLayout(new GridLayout(10, 8));

    	    JLabel productoNombreLabel = new JLabel("Nombre del producto:");
    	    productoNombreField = new JTextField();
    	    JLabel productoPorcionesLabel = new JLabel("Cantidad de porciones:");
    	    productoPorcionesField = new JTextField();
    	    JLabel productoPrecioLabel = new JLabel("Precio del producto:");
    	    productoPrecioField = new JTextField();

    	    JButton registrarButton = new JButton("Registrar");
    	    JButton borrarButton = new JButton("Borrar");
    	    JButton actualizarButton = new JButton("Actualizar");

    	    registrarButton.addActionListener(this);
    	    borrarButton.addActionListener(this);
    	    actualizarButton.addActionListener(this);

    	    panel.add(productoNombreLabel);
    	    panel.add(productoNombreField);
    	    panel.add(productoPorcionesLabel);
    	    panel.add(productoPorcionesField);
    	    panel.add(productoPrecioLabel);
    	    panel.add(productoPrecioField);
    	    panel.add(registrarButton);
    	    panel.add(borrarButton);
    	    panel.add(actualizarButton);

    	    return panel;
    	}
    

    private JPanel createFacturacionPanel() {
        JPanel panel = new JPanel();
        panel.setLayout(new GridLayout(10, 8));

        JLabel facturacionNITLabel = new JLabel("NIT:");
        facturacionNITField = new JTextField();
        JLabel facturacionDescripcionLabel = new JLabel("Descripción:");
        facturacionDescripcionField = new JTextField();
        JLabel facturacionCantidadLabel = new JLabel("Cantidad:");
        facturacionCantidadField = new JTextField();
        JLabel facturacionPrecioLabel = new JLabel("Precio:");
        facturacionPrecioField = new JTextField();

        JButton registrarButton = new JButton("Registrar");
	    JButton borrarButton = new JButton("Borrar");
	    JButton actualizarButton = new JButton("Actualizar");

	    registrarButton.addActionListener(this);
	    borrarButton.addActionListener(this);
	    actualizarButton.addActionListener(this);
	    
        panel.add(facturacionNITLabel);
        panel.add(facturacionNITField);
        panel.add(facturacionDescripcionLabel);
        panel.add(facturacionDescripcionField);
        panel.add(facturacionCantidadLabel);
        panel.add(facturacionCantidadField);
        panel.add(facturacionPrecioLabel);
        panel.add(facturacionPrecioField);
        panel.add(registrarButton);
	    panel.add(borrarButton);
	    panel.add(actualizarButton);


        return panel;
    }

    private JPanel createInventarioPanel() {
        JPanel panel = new JPanel();
        panel.setLayout(new GridLayout(10, 8));

        JLabel sobresDeCafeLabel = new JLabel("Cantidad de sobres de café:");
        sobresDeCafeField = new JTextField();
        JLabel librasDeAzucarLabel = new JLabel("Cantidad de libras de azúcar:");
        librasDeAzucarField = new JTextField();
        JLabel litrosDeLecheLabel = new JLabel("Cantidad de litros de leche:");
        litrosDeLecheField = new JTextField();

        JButton registrarButton = new JButton("Registrar");
	    JButton borrarButton = new JButton("Borrar");
	    JButton actualizarButton = new JButton("Actualizar");

	    registrarButton.addActionListener(this);
	    borrarButton.addActionListener(this);
	    actualizarButton.addActionListener(this);
	    
        panel.add(sobresDeCafeLabel);
        panel.add(sobresDeCafeField);
        panel.add(librasDeAzucarLabel);
        panel.add(librasDeAzucarField);
        panel.add(litrosDeLecheLabel);
        panel.add(litrosDeLecheField);
        panel.add(registrarButton);
	    panel.add(borrarButton);
	    panel.add(actualizarButton);

        return panel;
    }

    private JPanel createInformacionOrdenPanel() {
        JPanel panel = new JPanel();
        panel.setLayout(new GridLayout(10, 8));

        JLabel ordenCodigoLabel = new JLabel("Código de la orden:");
        ordenCodigoField = new JTextField();
        JLabel ordenVentaLabel = new JLabel("Venta realizada:");
        ordenVentaField = new JTextField();
        JLabel ordenVendedorLabel = new JLabel("Vendedor:");
        ordenVendedorField = new JTextField();
        
        JButton registrarButton = new JButton("Registrar");
	    JButton borrarButton = new JButton("Borrar");
	    JButton actualizarButton = new JButton("Actualizar");

	    registrarButton.addActionListener(this);
	    borrarButton.addActionListener(this);
	    actualizarButton.addActionListener(this);
	    

        panel.add(ordenCodigoLabel);
        panel.add(ordenCodigoField);
        panel.add(ordenVentaLabel);
        panel.add(ordenVentaField);
        panel.add(ordenVendedorLabel);
        panel.add(ordenVendedorField);
        panel.add(registrarButton);
	    panel.add(borrarButton);
	    panel.add(actualizarButton);

        

        return panel;
    }

    private JPanel createEmpleadoDelMesPanel() {
        JPanel panel = new JPanel();
        panel.setLayout(new GridLayout(10, 8));

        JLabel empleadoNombreLabel = new JLabel("Nombre del empleado:");
        empleadoNombreField = new JTextField();
        JLabel empleadoPuestoLabel = new JLabel("Puesto del empleado:");
        empleadoPuestoField = new JTextField();
        JLabel empleadoVentasLabel = new JLabel("Ventas del empleado:");
        empleadoVentasField = new JTextField();
        
        JButton registrarButton = new JButton("Registrar");
	    JButton borrarButton = new JButton("Borrar");
	    JButton actualizarButton = new JButton("Actualizar");

	    registrarButton.addActionListener(this);
	    borrarButton.addActionListener(this);
	    actualizarButton.addActionListener(this);
	    

        panel.add(empleadoNombreLabel);
        panel.add(empleadoNombreField);
        panel.add(empleadoPuestoLabel);
        panel.add(empleadoPuestoField);
        panel.add(empleadoVentasLabel);
        panel.add(empleadoVentasField);
        panel.add(registrarButton);
	    panel.add(borrarButton);
	    panel.add(actualizarButton);

        return panel;
    }
    
    
    

    @Override
    
    public void actionPerformed(ActionEvent e) {
        if (e.getActionCommand().equals("Registrar")) {
            // Lógica para registrar el producto en la base de datos
        } else if (e.getActionCommand().equals("Borrar")) {
            // Lógica para borrar el producto de la base de datos
        } else if (e.getActionCommand().equals("Actualizar")) {
            // Lógica para actualizar la información del producto en la base de datos
        }
    }
    }



public class CafeteriaApp {
    public static void main(String[] args) {
        Cafeteria cafeteria = new Cafeteria();

        SwingUtilities.invokeLater(() -> {
            CafeteriaAppGUI gui = new CafeteriaAppGUI(cafeteria);
            gui.setVisible(true);
        });
    }
}

import java.sql.Connection;

import java.sql.DriverManager;

import java.sql.ResultSet;

import java.sql.SQLException;

import java.sql.Statement;

public class ConexionMariaDB {

    public static void main(String[] args) {

        // Configuración de la conexión
	
        String url = "jdbc:mariadb://localhost:3306/cafeteria";
	
        String usuario = "root";
	
        String contraseña = "2004";

        // Intentar establecer la conexión
        try (Connection conexion = DriverManager.getConnection("jdbc:mariadb://localhost:3306/cafeteria", "root", "2004")) {
            System.out.println("Conexión exitosa");

            // Realizar una consulta simple
            Statement statement = conexion.createStatement();
            ResultSet resultSet = statement.executeQuery("SELECT * FROM tu_tabla");

            // Procesar los resultados
            while (resultSet.next()) {
                // Acceder a los datos, por ejemplo:
                String columna1 = resultSet.getString("nombre_columna1");
                int columna2 = resultSet.getInt("nombre_columna2");

                // Hacer algo con los datos
                System.out.println("Columna1: " + columna1 + ", Columna2: " + columna2);
            }
        } catch (SQLException e) {
            System.err.println("Error al conectar a la base de datos: " + e.getMessage());
        }
    }
}



import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class Producto {
    String nombre;
    double precio;

    public Producto(String nombre, double precio) {
        this.nombre = nombre;
        this.precio = precio;
    }
}

public class AdministracionCafeteria {
    private static List<Producto> menu = new ArrayList<>();
    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        char opcion;

        do {
            System.out.println("1. Alta de producto");
            System.out.println("2. Baja de producto");
            System.out.println("3. Actualización de producto");
            System.out.println("4. Mostrar menú");
            System.out.println("5. Salir");
            System.out.print("Seleccione una opción: ");
            opcion = scanner.next().charAt(0);

            switch (opcion) {
                case '1':
                    altaProducto();
                    break;
                case '2':
                    bajaProducto();
                    break;
                case '3':
                    actualizarProducto();
                    break;
                case '4':
                    mostrarMenu();
                    break;
                case '5':
                    System.out.println("¡Hasta luego!");
                    break;
                default:
                    System.out.println("Opción no válida. Por favor, seleccione nuevamente.");
            }
        } while (opcion != '5');
    }

    private static void altaProducto() {
        System.out.print("Ingrese el nombre del producto: ");
        String nombre = scanner.next();
        System.out.print("Ingrese el precio del producto: ");
        double precio = scanner.nextDouble();

        Producto nuevoProducto = new Producto(nombre, precio);
        menu.add(nuevoProducto);

        System.out.println("Producto agregado con éxito.");
    }

    private static void bajaProducto() {
        System.out.print("Ingrese el nombre del producto a dar de baja: ");
        String nombre = scanner.next();

        boolean productoEncontrado = false;
        for (Producto producto : menu) {
            if (producto.nombre.equalsIgnoreCase(nombre)) {
                menu.remove(producto);
                productoEncontrado = true;
                System.out.println("Producto eliminado con éxito.");
                break;
            }
        }

        if (!productoEncontrado) {
            System.out.println("Producto no encontrado. Verifique el nombre e intente nuevamente.");
        }
    }

    private static void actualizarProducto() {
        System.out.print("Ingrese el nombre del producto a actualizar: ");
        String nombre = scanner.next();

        boolean productoEncontrado = false;
        for (Producto producto : menu) {
            if (producto.nombre.equalsIgnoreCase(nombre)) {
                System.out.print("Ingrese el nuevo precio del producto: ");
                double nuevoPrecio = scanner.nextDouble();
                producto.precio = nuevoPrecio;
                productoEncontrado = true;
                System.out.println("Producto actualizado con éxito.");
                break;
            }
        }

        if (!productoEncontrado) {
            System.out.println("Producto no encontrado. Verifique el nombre e intente nuevamente.");
        }
    }

    private static void mostrarMenu() {
        System.out.println("Menú de la cafetería:");
        for (Producto producto : menu) {
            System.out.println("Nombre: " + producto.nombre + ", Precio: " + producto.precio);
        }
    }
}



CREATE TABLE Producto (cafeteria

    id INT AUTO_INCREMENT PRIMARY KEY,
    
    nombre VARCHAR(255) NOT NULL,
    
    porciones INT NOT NULL,
    
    precio DOUBLE NOT NULL
);

CREATE TABLE Facturacion (

    id INT AUTO_INCREMENT PRIMARY KEY,
    
    nit VARCHAR(20) NOT NULL,
    
    descripcion VARCHAR(255) NOT NULL,
    
    cantidad INT NOT NULL,
    
    precio DOUBLE NOT NULL
);

CREATE TABLE Inventario (

    id INT AUTO_INCREMENT PRIMARY KEY,
    
    sobres_cafe INT NOT NULL,
    
    libras_azucar INT NOT NULL,
    
    litros_leche INT NOT NULL
    
);
CREATE TABLE InformacionOrden (

    id INT AUTO_INCREMENT PRIMARY KEY,
    
    codigo VARCHAR(20) NOT NULL,
    
    venta_realizada VARCHAR(255) NOT NULL,
    
    vendedor VARCHAR(255) NOT NULL
);
CREATE TABLE EmpleadoDelMes (

    id INT AUTO_INCREMENT PRIMARY KEY,

    
    nombre VARCHAR(255) NOT NULL,
    
    puesto VARCHAR(255) NOT NULL,
    
    ventas INT NOT NULL
);
