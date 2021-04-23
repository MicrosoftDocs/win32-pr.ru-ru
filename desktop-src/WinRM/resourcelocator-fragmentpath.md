---
title: Свойство ResourceLocator. Фрагментпас (Всмандисп. h)
description: Возвращает или задает путь к фрагменту или свойству ресурса, когда ResourceLocator используется в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Фрагментпас
- Служба удаленного управления Windows свойства Фрагментпас, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, свойство Фрагментпас
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071663"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="9b30f-106">ResourceLocator. Фрагментпас, свойство</span><span class="sxs-lookup"><span data-stu-id="9b30f-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="9b30f-107">Возвращает или задает путь к [*фрагменту*](windows-remote-management-glossary.md) или свойству [*ресурса*](windows-remote-management-glossary.md) , когда [**ResourceLocator**](resourcelocator.md) используется в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="9b30f-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="9b30f-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9b30f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b30f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b30f-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="9b30f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9b30f-110">Property value</span></span>

<span data-ttu-id="9b30f-111">Строка, идентифицирующая фрагмент или свойство ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b30f-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="9b30f-112">Например, если ресурс является диском, а запрошенным свойством является Manufacturer, строка может содержать `Diskdrive/Manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="9b30f-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="9b30f-113">В тексте фрагмента учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="9b30f-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="9b30f-114">В этом случае нельзя использовать `diskdrive/manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="9b30f-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b30f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b30f-115">Remarks</span></span>

<span data-ttu-id="9b30f-116">**Ивсманресаурцелокатор:: фрагментпас** — соответствующее свойство C++.</span><span class="sxs-lookup"><span data-stu-id="9b30f-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="9b30f-117">Можно указать один элемент свойства массива, указав индекс массива, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9b30f-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="9b30f-118">Имейте в виду, что индексация массива начинается с 1, а не 0.</span><span class="sxs-lookup"><span data-stu-id="9b30f-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="9b30f-119">Чтобы получить весь массив, укажите имя свойства массива, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="9b30f-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="9b30f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9b30f-120">Requirements</span></span>



| <span data-ttu-id="9b30f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9b30f-121">Requirement</span></span> | <span data-ttu-id="9b30f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9b30f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b30f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b30f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9b30f-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b30f-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9b30f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b30f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9b30f-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b30f-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9b30f-127">Header</span><span class="sxs-lookup"><span data-stu-id="9b30f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b30f-128"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b30f-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b30f-129">IDL</span><span class="sxs-lookup"><span data-stu-id="9b30f-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b30f-130"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b30f-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b30f-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b30f-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b30f-132"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b30f-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b30f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9b30f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b30f-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b30f-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b30f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b30f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b30f-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="9b30f-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





