В объекта ориентированных языках используется следующая структура

![[oo-approach]]

Но так как **Go** является процедурным ЯП, то такая структура не может прижиться в нем, поэтому в нем используют эту структуру

![[go-approeach]]

В итоге получаем чтобы определить методы для нашего нового типа данных нужно создать функцию, и в качестве параметра передать в нее `receiver` этого типа.

```go
type Deck []string

func (d Deck) Print() {
	for _, card := range d {
		fmt.Println(card)
	}
}
```