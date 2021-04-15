---
description: Объект Компонентинфо представляет дополнительные сведения о компоненте, который можно получить с помощью вызова из Мсижеткомпонентпасекс.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Объект Компонентинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651885"
---
# <a name="componentinfo-object"></a><span data-ttu-id="479b3-103">Объект Компонентинфо</span><span class="sxs-lookup"><span data-stu-id="479b3-103">ComponentInfo object</span></span>

<span data-ttu-id="479b3-104">Объект Компонентинфо представляет дополнительные сведения о компоненте, который можно получить с помощью вызова из Мсижеткомпонентпасекс.</span><span class="sxs-lookup"><span data-stu-id="479b3-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="479b3-105">**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="479b3-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="479b3-106">Этот объект доступен, начиная с установщик Windows 5,0.</span><span class="sxs-lookup"><span data-stu-id="479b3-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="479b3-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="479b3-107">Members</span></span>

<span data-ttu-id="479b3-108">Объект **компонентинфо** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="479b3-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="479b3-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="479b3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="479b3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="479b3-110">Properties</span></span>

<span data-ttu-id="479b3-111">Объект **компонентинфо** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="479b3-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="479b3-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="479b3-112">Property</span></span>                                                        | <span data-ttu-id="479b3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="479b3-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="479b3-114">**компоненткоде**</span><span class="sxs-lookup"><span data-stu-id="479b3-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="479b3-115">Код компонента рассматриваемого компонента.</span><span class="sxs-lookup"><span data-stu-id="479b3-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="479b3-116">**Путь**</span><span class="sxs-lookup"><span data-stu-id="479b3-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="479b3-117">Путь к компоненту.</span><span class="sxs-lookup"><span data-stu-id="479b3-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="479b3-118">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="479b3-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="479b3-119">Состояние компонента.</span><span class="sxs-lookup"><span data-stu-id="479b3-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="479b3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="479b3-120">Requirements</span></span>



| <span data-ttu-id="479b3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="479b3-121">Requirement</span></span> | <span data-ttu-id="479b3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="479b3-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="479b3-123">Версия</span><span class="sxs-lookup"><span data-stu-id="479b3-123">Version</span></span><br/> | <span data-ttu-id="479b3-124">Установщик Windows 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="479b3-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="479b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="479b3-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="479b3-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="479b3-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="479b3-127">IID</span><span class="sxs-lookup"><span data-stu-id="479b3-127">IID</span></span><br/>     | <span data-ttu-id="479b3-128">IID \_ икомпонентинфо определен как 000C1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="479b3-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="479b3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="479b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="479b3-130">Использование интерфейса автоматизации</span><span class="sxs-lookup"><span data-stu-id="479b3-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="479b3-131">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="479b3-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




