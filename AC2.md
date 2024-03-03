ex 1:
package main

import "fmt"

func main() {
    var vetor [10]int
    var i int
    i = 0
    for i < 10 {
        fmt.Scan(&vetor[i])
        i++
    }
    i = 0
    for i < 10 {
        fmt.Println(vetor[i])
        i++
    }
}
ex 2:
package main

import "fmt"


func main() {
  var x string
  fmt.Scanln(&x)
  var lista = []rune(x)
  for i := len(lista) - 1; i  >= 0; i-- {
    fmt.Print(string(lista[i]))
  }
}

ex 3:
package main

import "fmt"
import "math"

type Ponto struct {
  X float64
  Y float64
}

func (p Ponto) DistanciaOrigem() float64 {
    return math.Sqrt(math.Pow(p.X, 2) + math.Pow(p.Y, 2))
}

func main() {
    ponto := Ponto{X: 1, Y: 2}
    fmt.Println("Distância até a origem:", ponto.DistanciaOrigem())
}


ex 4:
package geometria

type retangulo struct {
    x  float64
    y float64
}

func (r retangulo) area() float64 {
    return r.Altura * r.Largura
}

func (r retangulo) perimetro() float64 {
    return 2*r.x + 2*r.y
}
package main

import (
    "fmt"
    "geometria"
)

func main() {
    retangulo := geometria.retangulo{x: 10, y: 5}
    fmt.Println("area:", retangulo.area())
    fmt.Println("perimetro:", retangulo.perimetro())
}
