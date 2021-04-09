---
title: Метод WSMan. Креатеконнектионоптионс (Всмандисп. h)
description: Создает объект ConnectionOptions, который указывает имя пользователя и пароль, используемые при создании сеанса.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Креатеконнектионоптионс
- Служба удаленного управления Windows метода Креатеконнектионоптионс, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Креатеконнектионоптионс
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891665"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="07d3f-106">Метод WSMan. Креатеконнектионоптионс</span><span class="sxs-lookup"><span data-stu-id="07d3f-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="07d3f-107">Создает объект [**ConnectionOptions**](connectionoptions.md) , который указывает имя пользователя и пароль, используемые при создании сеанса.</span><span class="sxs-lookup"><span data-stu-id="07d3f-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d3f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07d3f-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="07d3f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07d3f-109">Parameters</span></span>

<span data-ttu-id="07d3f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="07d3f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07d3f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07d3f-111">Return value</span></span>

<span data-ttu-id="07d3f-112">Объект [**ConnectionOptions**](connectionoptions.md) , который используется для указания пары имя пользователя и пароль, которые используются для идентификации пользователя при проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="07d3f-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="07d3f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07d3f-113">Remarks</span></span>

<span data-ttu-id="07d3f-114">Для вызова этого метода используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="07d3f-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="07d3f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="07d3f-115">Requirements</span></span>



| <span data-ttu-id="07d3f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="07d3f-116">Requirement</span></span> | <span data-ttu-id="07d3f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="07d3f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d3f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07d3f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="07d3f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07d3f-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="07d3f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07d3f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="07d3f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07d3f-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="07d3f-122">Header</span><span class="sxs-lookup"><span data-stu-id="07d3f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d3f-123"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d3f-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="07d3f-124">IDL</span><span class="sxs-lookup"><span data-stu-id="07d3f-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07d3f-125"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="07d3f-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="07d3f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07d3f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="07d3f-127"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="07d3f-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="07d3f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="07d3f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d3f-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d3f-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07d3f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07d3f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d3f-131">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="07d3f-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="07d3f-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="07d3f-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





