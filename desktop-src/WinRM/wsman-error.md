---
title: Свойство WSMan. Error (Всмандисп. h)
description: Возвращает дополнительные сведения об ошибке в потоке XML для предыдущего вызова метода WSMan, если службе служба удаленного управления Windows не удалось создать объект сеанса, объект ConnectionOptions или объект ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства ошибки
- Служба удаленного управления Windows свойства ошибки, объект WSMan
- Объект WSMan служба удаленного управления Windows, свойство Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135982"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="5b077-106">WSMan. Error, свойство</span><span class="sxs-lookup"><span data-stu-id="5b077-106">WSMan.Error property</span></span>

<span data-ttu-id="5b077-107">Возвращает дополнительные сведения об ошибке в потоке XML для предыдущего вызова метода [**WSMan**](wsman.md) , если службе Служба удаленного управления Windows не удалось создать объект [**сеанса**](session.md) , объект [**ConnectionOptions**](connectionoptions.md) или объект [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5b077-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="5b077-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5b077-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b077-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b077-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="5b077-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5b077-110">Property value</span></span>

<span data-ttu-id="5b077-111">XML-представление сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5b077-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b077-112">Требования</span><span class="sxs-lookup"><span data-stu-id="5b077-112">Requirements</span></span>



| <span data-ttu-id="5b077-113">Требование</span><span class="sxs-lookup"><span data-stu-id="5b077-113">Requirement</span></span> | <span data-ttu-id="5b077-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5b077-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b077-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b077-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5b077-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b077-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5b077-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b077-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5b077-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b077-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5b077-119">Header</span><span class="sxs-lookup"><span data-stu-id="5b077-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b077-120"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b077-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b077-121">IDL</span><span class="sxs-lookup"><span data-stu-id="5b077-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b077-122"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b077-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5b077-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b077-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b077-124"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5b077-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5b077-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5b077-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b077-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b077-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5b077-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b077-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b077-128">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="5b077-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





