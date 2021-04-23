---
title: ResourceLocator. Аддселектор, метод (Всмандисп. h)
description: Добавляет селектор в объект ResourceLocator. Селектор указывает конкретный экземпляр ресурса.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Аддселектор
- Служба удаленного управления Windows метода Аддселектор, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, метод Аддселектор
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988703"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="d9df2-107">ResourceLocator. Аддселектор, метод</span><span class="sxs-lookup"><span data-stu-id="d9df2-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="d9df2-108">Добавляет [*селектор*](windows-remote-management-glossary.md) в объект [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="d9df2-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="d9df2-109">Селектор указывает конкретный экземпляр *ресурса*.</span><span class="sxs-lookup"><span data-stu-id="d9df2-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="d9df2-110">Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="d9df2-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9df2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9df2-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="d9df2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9df2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9df2-113">*ресаурцеселнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9df2-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9df2-114">Имя селектора.</span><span class="sxs-lookup"><span data-stu-id="d9df2-114">The selector name.</span></span> <span data-ttu-id="d9df2-115">Например, при запросе данных WMI этот параметр является ключевым свойством класса WMI.</span><span class="sxs-lookup"><span data-stu-id="d9df2-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="d9df2-116">*селвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9df2-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9df2-117">Значение селектора.</span><span class="sxs-lookup"><span data-stu-id="d9df2-117">The selector value.</span></span> <span data-ttu-id="d9df2-118">Например, для данных WMI этот параметр содержит значение для ключевого свойства, идентифицирующего конкретный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="d9df2-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9df2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9df2-119">Remarks</span></span>

<span data-ttu-id="d9df2-120">**Ивсманресаурцелокатор:: аддселектор** — соответствующий метод C++.</span><span class="sxs-lookup"><span data-stu-id="d9df2-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9df2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d9df2-121">Requirements</span></span>



| <span data-ttu-id="d9df2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d9df2-122">Requirement</span></span> | <span data-ttu-id="d9df2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d9df2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9df2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9df2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9df2-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9df2-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d9df2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9df2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9df2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9df2-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d9df2-128">Header</span><span class="sxs-lookup"><span data-stu-id="d9df2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9df2-129"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9df2-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9df2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d9df2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d9df2-131"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9df2-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d9df2-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9df2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9df2-133"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9df2-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9df2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d9df2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9df2-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9df2-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9df2-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9df2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9df2-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="d9df2-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





