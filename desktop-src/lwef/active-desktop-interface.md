---
title: Использование объекта Active Desktop
description: эта статья содержит сведения об объекте активедесктоп, который входит в состав API оболочки Windows. Этот объект через его интерфейс Иактиведесктоп позволяет добавлять, удалять и изменять элементы на рабочем столе.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Объект Активедесктоп
- Активный рабочий стол
- Перечисление, элементы рабочего стола
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6daf1b5fbc73286619f07c8af76fbbce53bcaa8962cc88cf20f5af74bbdec82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610664"
---
# <a name="using-the-active-desktop-object"></a>Использование объекта Active Desktop

\[эта функция поддерживается только в Windows XP и более ранних версиях. \]

эта статья содержит сведения об объекте **активедесктоп** , который входит в состав API оболочки Windows. Этот объект через его интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) позволяет добавлять, удалять и изменять элементы на рабочем столе.

## <a name="overview-of-the-active-desktop-interface"></a>Общие сведения о интерфейсе Active Desktop

-   [Доступ к активному рабочему столу](#accessing-the-active-desktop)
-   [Добавление элемента рабочего стола](#adding-a-desktop-item)
-   [Перечисление элементов рабочего стола](#enumerating-the-desktop-items)

Active Desktop — это функция, появившаяся в Microsoft Internet Explorer 4,0, позволяющая включать HTML-документы и элементы (например, элементы управления Microsoft ActiveX и java-приложения) непосредственно на рабочий стол. интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , который является частью API оболочки Windows, используется для программного добавления, удаления и изменения элементов на рабочем столе. Элементы Active Desktop также можно добавить с помощью файла формата определения канала (CDF).

### <a name="accessing-the-active-desktop"></a>Доступ к активному рабочему столу

Чтобы получить доступ к Active Desktop, клиентскому приложению потребуется создать экземпляр объекта Активедесктоп (CLSID \_ активедесктоп) с функцией [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) и получить указатель на интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) объекта.

В следующем примере показано, как получить указатель на интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>Добавление элемента рабочего стола

Добавить элемент рабочего стола можно с помощью трех методов: [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**Иактиведесктоп:: адддесктопитемвисуи**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)и [**иактиведесктоп:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Каждый элемент рабочего стола, добавляемый к активному рабочему столу, должен иметь другой исходный URL-адрес.

Методы [**иактиведесктоп:: адддесктопитемвисуи**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) и [**Иактиведесктоп:: аддурл**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) предоставляют возможность отображения различных пользовательских интерфейсов, которые можно отобразить перед добавлением элемента рабочего стола на активный рабочий стол. Интерфейсы проверяют, хотят ли пользователи добавить элемент рабочего стола в рабочий стол Active Desktop. Кроме того, интерфейсы уведомляют пользователей о любых угрозах безопасности, которые гарантируют параметры зоны безопасности URL-адресов, и запрашивают у пользователей возможность создания подписки для этого элемента рабочего стола. Оба метода также предоставляют способ подавления пользовательских интерфейсов. Для обновления реестра метод [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) требует вызова [**Иактиведесктоп:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) . Для **иактиведесктоп:: адддесктопитемвисуи** клиентское приложение должно немедленно освободить интерфейс [**иактиведесктоп**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , а затем использовать функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения интерфейса к экземпляру объекта **активедесктоп** , включающего только что добавленный элемент рабочего стола.

Метод [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) добавляет указанный элемент рабочего стола в активный рабочий стол без какого-либо пользовательского интерфейса, если это не мешает параметрам зоны безопасности URL. Если параметры зоны безопасности URL-адреса не допускают Добавление элемента рабочего стола без запроса пользователя, то метод завершается ошибкой. Для обновления реестра **иактиведесктоп:: адддесктопитем** также требуется вызов [**Иактиведесктоп:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) .

В следующем примере показано, как добавить элемент Desktop с помощью метода [**иактиведесктоп:: адддесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>Перечисление элементов рабочего стола

Чтобы перечислить элементы рабочего стола, установленные в настоящий момент на активном рабочем столе, клиентскому приложению необходимо получить общее число элементов рабочего стола, установленных с помощью метода [**иактиведесктоп:: жетдесктопитемкаунт**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) , а затем создать цикл, извлекающий структуру [**компонентов**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) для каждого элемента рабочего стола, вызвав метод [**иактиведесктоп:: жетдесктопитем**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) , используя индекс элемента рабочего стола.

В следующем примере демонстрируется один из способов перечисления элементов рабочего стола.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 