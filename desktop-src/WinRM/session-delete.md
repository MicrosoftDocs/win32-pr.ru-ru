---
title: Метод Session. redelete (Всмандисп. h)
description: Удаляет ресурс, указанный в URI ресурса.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Delete
- Служба удаленного управления Windows метода Delete, объект Session
- Объект Session служба удаленного управления Windows, метод Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988386"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="28d7f-106">Session. redelete, метод</span><span class="sxs-lookup"><span data-stu-id="28d7f-106">Session.Delete method</span></span>

<span data-ttu-id="28d7f-107">Удаляет ресурс, указанный в URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="28d7f-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d7f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28d7f-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="28d7f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28d7f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28d7f-110">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28d7f-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28d7f-111">URI ресурса, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="28d7f-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="28d7f-112">Для указания ресурса можно также использовать объект [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="28d7f-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="28d7f-113">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="28d7f-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28d7f-114">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="28d7f-114">Reserved for future use.</span></span> <span data-ttu-id="28d7f-115">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="28d7f-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28d7f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28d7f-116">Return value</span></span>

<span data-ttu-id="28d7f-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="28d7f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d7f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28d7f-118">Remarks</span></span>

<span data-ttu-id="28d7f-119">Для вызова этого метода используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="28d7f-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="28d7f-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="28d7f-120">Examples</span></span>

<span data-ttu-id="28d7f-121">В следующем примере кода VBScript удаляются прослушиватели, настроенные для транспорта HTTP.</span><span class="sxs-lookup"><span data-stu-id="28d7f-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="28d7f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="28d7f-122">Requirements</span></span>



| <span data-ttu-id="28d7f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="28d7f-123">Requirement</span></span> | <span data-ttu-id="28d7f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="28d7f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28d7f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28d7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="28d7f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28d7f-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="28d7f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28d7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="28d7f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28d7f-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="28d7f-129">Header</span><span class="sxs-lookup"><span data-stu-id="28d7f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d7f-130"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d7f-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="28d7f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="28d7f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28d7f-132"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28d7f-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="28d7f-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28d7f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="28d7f-134"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="28d7f-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="28d7f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="28d7f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28d7f-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28d7f-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28d7f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28d7f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d7f-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="28d7f-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





