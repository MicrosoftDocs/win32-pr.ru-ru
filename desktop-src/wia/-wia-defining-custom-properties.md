---
description: Определение пользовательских свойств.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Определение пользовательских свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693080"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="f8a16-103">Определение пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="f8a16-103">Defining Custom Properties</span></span>

<span data-ttu-id="f8a16-104">**Определение пользовательских свойств**.</span><span class="sxs-lookup"><span data-stu-id="f8a16-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="f8a16-105">Если требуется для определения пользовательских свойств в минидривере получения образа Windows (WIA), \_ \_ необходимо использовать свойство WIA Private девпроп для настраиваемых свойств корневого элемента, а \_ свойство WIA Private \_ итемпроп — для других свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="f8a16-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="f8a16-106">Эти константы определены в *виадеф. h*.</span><span class="sxs-lookup"><span data-stu-id="f8a16-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="f8a16-107">В следующем примере кода показаны определения для трех свойств корневого элемента.</span><span class="sxs-lookup"><span data-stu-id="f8a16-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="f8a16-108">Идентификатор свойства для первого настраиваемого свойства корневого элемента, НАСТРАИВАЕМого \_ root \_ prop \_ 1, определяется в терминах \_ частного \_ девпроп WIA.</span><span class="sxs-lookup"><span data-stu-id="f8a16-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="f8a16-109">Идентификаторы свойств для дополнительных свойств корневого элемента определяются в терминах "WIA \_ Private \_ девпроп + 1", WIA \_ Private \_ девпроп + 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="f8a16-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="f8a16-110">Шаблон можно продолжить, если требуются дополнительные свойства настраиваемого корневого элемента.</span><span class="sxs-lookup"><span data-stu-id="f8a16-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="f8a16-111">В следующем примере показаны определения для трех свойств настраиваемых дочерних элементов и идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="f8a16-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="f8a16-112">Идентификатор свойства для первого настраиваемого свойства дочернего элемента с НАСТРАИВАЕМым \_ дочерним элементом \_ prop \_ 1 определяется в терминах \_ Private \_ итемпроп WIA.</span><span class="sxs-lookup"><span data-stu-id="f8a16-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="f8a16-113">Идентификаторы свойств для дополнительных свойств дочерних элементов определяются с точки зрения WIA \_ Private \_ итемпроп + 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="f8a16-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="f8a16-114">Как и ранее, шаблон можно продолжить, если требуются дополнительные свойства настраиваемого дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="f8a16-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="f8a16-115">Настраиваемые свойства WIA должны иметь пользовательские имена свойств, связанные с идентификаторами настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="f8a16-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="f8a16-116">В следующем примере кода показаны определения для трех настраиваемых имен свойств корневого элемента.</span><span class="sxs-lookup"><span data-stu-id="f8a16-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="f8a16-117">(Эти имена свойств используются с идентификаторами настраиваемых свойств, которые были созданы в предыдущем примере, где имя пользовательского свойства содержится в ПОЛЬЗОВАТЕЛЬСКОМ \_ \_Строка root Prop \_ 1 \_ связана с пользовательским корневым свойством элемента с идентификатором пользовательской \_ корневой настройки \_ prop \_ 1.)</span><span class="sxs-lookup"><span data-stu-id="f8a16-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="f8a16-118">Имена свойств WIA *не* локализуются на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="f8a16-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="f8a16-119">Это обусловлено тем, что свойства WIA могут быть прочитаны приложениями с помощью идентификатора свойства или имени свойства.</span><span class="sxs-lookup"><span data-stu-id="f8a16-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="f8a16-120">Если используется имя, оно должно быть константой, точно так же, как идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="f8a16-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 



