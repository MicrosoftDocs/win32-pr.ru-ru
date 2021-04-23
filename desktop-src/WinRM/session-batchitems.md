---
title: Session.Batсвойство Читемс (Всмандисп. h)
description: Задает и возвращает количество элементов в каждом пакете перечисления.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Батчитемс
- Служба удаленного управления Windows свойства Батчитемс, объект Session
- Объект Session служба удаленного управления Windows, свойство Батчитемс
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710520"
---
# <a name="sessionbatchitems-property"></a><span data-ttu-id="f6663-106">Session.Bat, свойство Читемс</span><span class="sxs-lookup"><span data-stu-id="f6663-106">Session.BatchItems property</span></span>

<span data-ttu-id="f6663-107">Задает и возвращает количество элементов в каждом пакете перечисления.</span><span class="sxs-lookup"><span data-stu-id="f6663-107">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="f6663-108">Это значение нельзя изменить во время перечисления.</span><span class="sxs-lookup"><span data-stu-id="f6663-108">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="f6663-109">Поставщик ресурсов может установить ограничение.</span><span class="sxs-lookup"><span data-stu-id="f6663-109">The resource provider may set a limit.</span></span>

<span data-ttu-id="f6663-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f6663-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6663-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6663-111">Syntax</span></span>


```VB
Session.BatchItems As long
```



## <a name="property-value"></a><span data-ttu-id="f6663-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f6663-112">Property value</span></span>

<span data-ttu-id="f6663-113">Указывает максимальное количество элементов, возвращаемых для каждого базового сетевого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f6663-113">Specifies the maximum number of elements returned for each underlying network call to the service.</span></span> <span data-ttu-id="f6663-114">Значение по умолчанию равно 20.</span><span class="sxs-lookup"><span data-stu-id="f6663-114">The default is 20.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6663-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6663-115">Remarks</span></span>

<span data-ttu-id="f6663-116">Это функция оптимизации, которая управляет частотой сетевых вызовов между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="f6663-116">This is an optimization feature that controls how often network calls are made between the client and the server.</span></span> <span data-ttu-id="f6663-117">В настоящее время он используется только для перечислений.</span><span class="sxs-lookup"><span data-stu-id="f6663-117">Currently, it is used only for enumerations.</span></span> <span data-ttu-id="f6663-118">Дополнительные сведения о перечислении ресурсов см. в разделе [**Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="f6663-118">For more information about enumerating resources, see [**Enumerate**](session-enumerate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6663-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f6663-119">Requirements</span></span>



| <span data-ttu-id="f6663-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f6663-120">Requirement</span></span> | <span data-ttu-id="f6663-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f6663-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6663-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6663-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6663-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6663-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f6663-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6663-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6663-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6663-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f6663-126">Header</span><span class="sxs-lookup"><span data-stu-id="f6663-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6663-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6663-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6663-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f6663-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6663-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6663-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f6663-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6663-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6663-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f6663-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f6663-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f6663-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6663-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6663-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6663-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6663-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6663-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="f6663-135">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="f6663-136">**Перечислить**</span><span class="sxs-lookup"><span data-stu-id="f6663-136">**Enumerate**</span></span>](session-enumerate.md)
</dt> <dt>

[<span data-ttu-id="f6663-137">**Enumerator. ReadItem**</span><span class="sxs-lookup"><span data-stu-id="f6663-137">**Enumerator.ReadItem**</span></span>](enumerator-readitem.md)
</dt> </dl>

 

 





