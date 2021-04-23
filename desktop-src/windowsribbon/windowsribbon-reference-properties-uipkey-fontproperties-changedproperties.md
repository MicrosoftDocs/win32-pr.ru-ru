---
title: UI_PKEY_FontProperties_ChangedProperties
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413414"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a><span data-ttu-id="a64ed-103">UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес</span><span class="sxs-lookup"><span data-stu-id="a64ed-103">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>

<span data-ttu-id="a64ed-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес.</span><span class="sxs-lookup"><span data-stu-id="a64ed-104">Identifies the UI\_PKEY\_FontProperties\_ChangedProperties property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a><span data-ttu-id="a64ed-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a64ed-105">Remarks</span></span>

<span data-ttu-id="a64ed-106">UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес используется приложением для запроса только измененных свойств из [UI \_ PKEY \_ фонтпропертиес](windowsribbon-reference-properties-uipkey-fontproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a64ed-106">UI\_PKEY\_FontProperties\_ChangedProperties is used by an application to query only changed properties from [UI\_PKEY\_FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span></span>

<span data-ttu-id="a64ed-107">Вызов метода [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) для этого объекта [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) возвращает [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="a64ed-107">Calling the [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method on this [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object returns an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

<span data-ttu-id="a64ed-108">UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес передается как последний параметр вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) в ведущее приложение ленты.</span><span class="sxs-lookup"><span data-stu-id="a64ed-108">UI\_PKEY\_FontProperties\_ChangedProperties is passed as the last parameter of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) call to the Ribbon host application.</span></span>

<span data-ttu-id="a64ed-109">Этот ключ свойства доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a64ed-109">This property key is read-only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a64ed-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a64ed-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a64ed-111">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="a64ed-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="a64ed-112">**иуисимплепропертисет**</span><span class="sxs-lookup"><span data-stu-id="a64ed-112">**IUISimplePropertySet**</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[<span data-ttu-id="a64ed-113">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="a64ed-113">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 