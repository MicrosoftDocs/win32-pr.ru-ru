---
title: Табграуп, элемент
description: Представляет контекстный набор элементов управления "Вкладка".
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- элемент табграуп Windows лента
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e2801ae8726fe10933b45e592e6f633f6455ea
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622100"
---
# <a name="tabgroup-element"></a>Табграуп, элемент

Представляет контекстный набор элементов управления ["Вкладка"](windowsribbon-controls-tabgroup.md) .

## <a name="usage"></a>Использование

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                             | Описание                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Вкладка**](windowsribbon-element-tab.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                 |
|-----------------------------------------------------------------------------------------|
| [**Лента. Контекстуалтабс**](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Должен быть хотя бы один раз для каждого элемента [**Ribbon. контекстуалтабс**](windowsribbon-element-ribbon-contextualtabs.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **табграуп** .

В этом разделе кода показано объявление команды **табграуп** с двумя контекстными вкладками.


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



В этом разделе кода показаны соответствующие объявления элементов управления **табграуп** .


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="element-information"></a>Сведения об элементе

- **минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: нет



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления группы вкладок](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[Элемент управления табуляции](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





