<script>
  // puede contener variables y funciones
  class User {
    // asigar propiedades mediante el constructor
    constructor(name, age) {
      this.name = name
      this.age = age
    }

    // Method
    showInfo() {
      console.log(this.name)
    }
  }

  // instanciar un nuevo User
  const carlos = new User('John', 30)

  carlos.showInfo()
</script>

<p>{carlos.name}</p>