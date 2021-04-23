---
description: дисплайпровидернаме
MS-HAID: WWAN\_profile\_v2.element\_DisplayProviderName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: дисплайпровидернаме
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 906f844d483789decb88a9d97fca083ef10f5550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072725"
---
# <a name="span-idwwan_profile_v2element_displayprovidernamespandisplayprovidername"></a><span data-ttu-id="9885c-103"><span id="WWAN_profile_v2.element_DisplayProviderName"></span>дисплайпровидернаме</span><span class="sxs-lookup"><span data-stu-id="9885c-103"><span id="WWAN_profile_v2.element_DisplayProviderName"></span>DisplayProviderName</span></span>

<span data-ttu-id="9885c-104">Элемент [**дисплайпровидернаме**](element-displayprovidername.md) является необязательным [**провидернаметипе**](./schema-providernametype-simpletype.md) , который содержит имя сетевого подключения, отображаемое в диспетчере подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="9885c-104">The [**DisplayProviderName**](element-displayprovidername.md) element is an optional [**providerNameType**](./schema-providernametype-simpletype.md) that contains the network connection name to display in the Windows Connection Manager.</span></span> <span data-ttu-id="9885c-105">Это имя будет отображаться только в том случае, если подписчик находится в домашней сети, а не в роуминге.</span><span class="sxs-lookup"><span data-stu-id="9885c-105">This name will only be displayed if the subscriber is on a home network and not roaming.</span></span> <span data-ttu-id="9885c-106">Имя сети роуминга отображается на основе информации с устройства мобильной широкополосной связи.</span><span class="sxs-lookup"><span data-stu-id="9885c-106">The roaming network name is displayed based on information from the mobile broadband device.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="9885c-107">Иерархия элементов</span><span class="sxs-lookup"><span data-stu-id="9885c-107">Element hierarchy</span></span>

**<DisplayProviderName>**

## <a name="syntax"></a><span data-ttu-id="9885c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9885c-108">Syntax</span></span>

``` syntax
<DisplayProviderName>

  providerNameType

</DisplayProviderName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="9885c-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы</span><span class="sxs-lookup"><span data-stu-id="9885c-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="9885c-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9885c-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="9885c-111">Нет.</span><span class="sxs-lookup"><span data-stu-id="9885c-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="9885c-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9885c-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="9885c-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="9885c-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="9885c-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9885c-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="9885c-115">Этот внешний элемент (Document) не может содержаться в каких-либо других элементах.</span><span class="sxs-lookup"><span data-stu-id="9885c-115">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="9885c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9885c-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9885c-117">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9885c-117">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v2</p></td>
</tr>
</tbody>
</table>

 

 
