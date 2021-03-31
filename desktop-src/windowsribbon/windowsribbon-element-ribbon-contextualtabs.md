---
title: Свойство Ribbon. Контекстуалтабс
description: Представляет контейнер для контекстных вкладок.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Лента Windows свойства Ribbon. Контекстуалтабс
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801552"
---
# <a name="ribboncontextualtabs-property"></a>Свойство Ribbon. Контекстуалтабс

Представляет контейнер для контекстных вкладок.

## <a name="usage"></a>Использование

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                       | Описание                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [**Группа вкладок**](windowsribbon-element-tabgroup.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                   |
|-----------------------------------------------------------|
| [**Лента**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждой [**ленты**](windowsribbon-element-ribbon.md).

Контекстные вкладки удобно использовать для отображения функциональных возможностей, относящихся только к конкретному контексту приложения, например к вкладке Формат изображения в текстовом редакторе, который отображается только при выделении изображения. Как правило, контекстные вкладки невидимы до тех пор, пока не происходит конкретный контекст приложения, и приложение уведомляет платформу Ribbon.

При отображении контекстные вкладки имеют цветовую кодировку, чтобы отличать их от обычных вкладок.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **Ribbon. контекстуалтабс** .

В этом разделе кода показано объявление команды [**табграуп**](windowsribbon-element-tabgroup.md) и два объявления команды контекстной [**вкладки**](windowsribbon-element-tab.md) .


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



В этом разделе кода показано объявление элемента управления **Ribbon. контекстуалтабс** с помощью [**табграуп**](windowsribbon-element-tabgroup.md) и двух элементов управления контекстной [**вкладки**](windowsribbon-element-tab.md) .


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Лента. вкладки**](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





