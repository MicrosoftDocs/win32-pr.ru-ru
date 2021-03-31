---
title: Файл_журнала. Item, свойство
description: Извлекает указанный экземпляр Логфилеитем из коллекции.
ms.assetid: 518c1343-f659-4434-910c-958c09ffab6a
keywords:
- Свойство элемента Сисмон
- Свойство Item Сисмон, класс LogFile
- Файл_журнала класса Сисмон, свойство Item
topic_type:
- apiref
api_name:
- LogFiles.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85af003cd6c0291ec90d17906f249726dfd526f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071356"
---
# <a name="logfilesitem-property"></a><span data-ttu-id="f1a9a-106">Файл_журнала. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="f1a9a-106">LogFiles.Item property</span></span>

<span data-ttu-id="f1a9a-107">Извлекает указанный экземпляр [**логфилеитем**](logfileitem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="f1a9a-107">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

<span data-ttu-id="f1a9a-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f1a9a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a9a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1a9a-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As LogFileItem
```



## <a name="property-value"></a><span data-ttu-id="f1a9a-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f1a9a-110">Property value</span></span>

<span data-ttu-id="f1a9a-111">Экземпляр [**логфилеитем**](logfileitem.md) , соответствующий указанному значению индекса.</span><span class="sxs-lookup"><span data-stu-id="f1a9a-111">[**LogFileItem**](logfileitem.md) instance that corresponds to the specified index value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a9a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1a9a-112">Remarks</span></span>

<span data-ttu-id="f1a9a-113">Это свойство по умолчанию для объекта [**файл_журнала**](systemmonitor-logfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="f1a9a-113">This is the default property of the [**LogFiles**](systemmonitor-logfiles.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a9a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f1a9a-114">Requirements</span></span>



| <span data-ttu-id="f1a9a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f1a9a-115">Requirement</span></span> | <span data-ttu-id="f1a9a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f1a9a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a9a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1a9a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a9a-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1a9a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f1a9a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1a9a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a9a-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1a9a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1a9a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f1a9a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1a9a-122"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f1a9a-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a9a-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1a9a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a9a-124">LogFiles</span><span class="sxs-lookup"><span data-stu-id="f1a9a-124">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="f1a9a-125">**логфилеитем**</span><span class="sxs-lookup"><span data-stu-id="f1a9a-125">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="f1a9a-126">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="f1a9a-126">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





