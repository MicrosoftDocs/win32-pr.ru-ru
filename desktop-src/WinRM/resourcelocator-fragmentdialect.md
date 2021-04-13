---
title: Свойство ResourceLocator. Фрагментдиалект (Всмандисп. h)
description: Возвращает или задает диалект языка для диалекта фрагмента ресурса, когда ResourceLocator используется в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Фрагментдиалект
- Служба удаленного управления Windows свойства Фрагментдиалект, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, свойство Фрагментдиалект
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492675"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="6208e-106">ResourceLocator. Фрагментдиалект, свойство</span><span class="sxs-lookup"><span data-stu-id="6208e-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="6208e-107">Возвращает или задает диалект языка для *диалекта* [*фрагмента*](windows-remote-management-glossary.md) [*ресурса*](windows-remote-management-glossary.md) , когда [**ResourceLocator**](resourcelocator.md) используется в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="6208e-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="6208e-108">Фрагмент представляет одно свойство или часть ресурса.</span><span class="sxs-lookup"><span data-stu-id="6208e-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="6208e-109">Вместо указания URI ресурса в операциях с объектами [**сеанса**](session.md) можно предоставить объект [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="6208e-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="6208e-110">Диалект указывает, какой язык XML описывает фрагмент для службы, которая реализует [протокол WS-Management](ws-management-protocol.md) и получает запрос.</span><span class="sxs-lookup"><span data-stu-id="6208e-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="6208e-111">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6208e-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6208e-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6208e-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="6208e-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6208e-113">Property value</span></span>

<span data-ttu-id="6208e-114">XML-строка, идентифицирующая язык, используемый в свойстве [**фрагментпас**](resourcelocator-fragmentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="6208e-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="6208e-115">Строка диалекта по умолчанию имеет спецификацию XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="6208e-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="6208e-116">Дополнительные сведения см. на веб-сайте [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="6208e-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="6208e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6208e-117">Remarks</span></span>

<span data-ttu-id="6208e-118">[**Ивсманресаурцелокатор:: фрагментдиалект**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) — соответствующее свойство C++.</span><span class="sxs-lookup"><span data-stu-id="6208e-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6208e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6208e-119">Requirements</span></span>



| <span data-ttu-id="6208e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6208e-120">Requirement</span></span> | <span data-ttu-id="6208e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6208e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6208e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6208e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6208e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6208e-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6208e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6208e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6208e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6208e-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6208e-126">Header</span><span class="sxs-lookup"><span data-stu-id="6208e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6208e-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6208e-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6208e-128">IDL</span><span class="sxs-lookup"><span data-stu-id="6208e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6208e-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6208e-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6208e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6208e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6208e-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6208e-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6208e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6208e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6208e-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6208e-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6208e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6208e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6208e-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="6208e-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





