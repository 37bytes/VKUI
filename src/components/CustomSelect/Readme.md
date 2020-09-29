Надстройка над `SelectMimicry`. Компонент принимает все валидные для этого элемента свойства + options

```jsx
class Example extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      value: '0',
      options: new Array(20).fill({}).map((item, index) => ({ label: String(index), value: String(index) }))
    }
  }

  render() {
    return (
      <View activePanel="сustomSelect">
        <Panel id="сustomSelect">
          <PanelHeader>
            CustomSelect
          </PanelHeader>
            <FormItem>
              <CustomSelect
                placeholder="Не выбрано"
                options={this.state.options}
                value={this.state.value}
                onChange={(option) => this.setState({ value: option.value })}
              />
            </FormItem>
        </Panel>
      </View>
    )
  }
}

<Example />
```
