---
title: Свойство ResourceLocator. ResourceURI (Всмандисп. h)
description: Возвращает или задает URI ресурса в объекте ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceURI, свойство служба удаленного управления Windows
- ResourceURI, свойство служба удаленного управления Windows, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, свойство ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491580"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="70b9a-106">ResourceLocator. ResourceURI, свойство</span><span class="sxs-lookup"><span data-stu-id="70b9a-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="70b9a-107">Возвращает или задает [*URI ресурса*](windows-remote-management-glossary.md) в объекте [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="70b9a-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="70b9a-108">Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="70b9a-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="70b9a-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="70b9a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b9a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70b9a-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="70b9a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70b9a-111">Property value</span></span>

<span data-ttu-id="70b9a-112">Строка, идентифицирующая ресурс.</span><span class="sxs-lookup"><span data-stu-id="70b9a-112">A string that identifies the resource.</span></span> <span data-ttu-id="70b9a-113">При задании универсального кода ресурса (URI) для объекта [**RESOURCELOCATOR**](resourcelocator.md) URI должен содержать только путь.</span><span class="sxs-lookup"><span data-stu-id="70b9a-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="70b9a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70b9a-114">Remarks</span></span>

<span data-ttu-id="70b9a-115">Ниже приведен пример правильного пути для [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span><span class="sxs-lookup"><span data-stu-id="70b9a-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="70b9a-116">Следующий путь не работает, так как он содержит ключ для конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="70b9a-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="70b9a-117">Используйте метод [**ResourceLocator. аддселектор**](resourcelocator-addselector.md) , чтобы указать конкретный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="70b9a-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="70b9a-118">**Ивсманресаурцелокатор:: resourceUri** — соответствующий метод C++.</span><span class="sxs-lookup"><span data-stu-id="70b9a-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b9a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="70b9a-119">Requirements</span></span>



| <span data-ttu-id="70b9a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="70b9a-120">Requirement</span></span> | <span data-ttu-id="70b9a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="70b9a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b9a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70b9a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="70b9a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70b9a-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="70b9a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70b9a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="70b9a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70b9a-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="70b9a-126">Header</span><span class="sxs-lookup"><span data-stu-id="70b9a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b9a-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="70b9a-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="70b9a-128">IDL</span><span class="sxs-lookup"><span data-stu-id="70b9a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70b9a-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70b9a-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="70b9a-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="70b9a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="70b9a-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70b9a-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70b9a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="70b9a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b9a-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70b9a-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70b9a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70b9a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b9a-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="70b9a-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





