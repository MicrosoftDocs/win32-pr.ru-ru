---
description: Метод DeleteAll объекта Свбемпривилежесет удаляет все привилегии из коллекции, тем самым удаляя его.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: Свбемпривилежесет. DeleteAll, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693500"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="7d119-103">Свбемпривилежесет. DeleteAll, метод</span><span class="sxs-lookup"><span data-stu-id="7d119-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="7d119-104">Метод **DeleteAll** объекта [**свбемпривилежесет**](swbemprivilegeset.md) удаляет все привилегии из коллекции, тем самым удаляя его.</span><span class="sxs-lookup"><span data-stu-id="7d119-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d119-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d119-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="7d119-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d119-106">Parameters</span></span>

<span data-ttu-id="7d119-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7d119-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d119-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d119-108">Return value</span></span>

<span data-ttu-id="7d119-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7d119-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7d119-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7d119-110">Error codes</span></span>

<span data-ttu-id="7d119-111">После завершения метода **DeleteAll** объект **Err** может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7d119-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="7d119-112">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7d119-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7d119-113">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7d119-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d119-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7d119-114">Requirements</span></span>



| <span data-ttu-id="7d119-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7d119-115">Requirement</span></span> | <span data-ttu-id="7d119-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7d119-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d119-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d119-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d119-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d119-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d119-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d119-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d119-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d119-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d119-121">Header</span><span class="sxs-lookup"><span data-stu-id="7d119-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d119-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d119-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d119-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7d119-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d119-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7d119-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7d119-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7d119-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d119-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d119-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d119-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="7d119-127">CLSID</span></span><br/>                    | <span data-ttu-id="7d119-128">\_СВБЕМПРИВИЛЕЖЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="7d119-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="7d119-129">IID</span><span class="sxs-lookup"><span data-stu-id="7d119-129">IID</span></span><br/>                      | <span data-ttu-id="7d119-130">IID \_ исвбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="7d119-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="7d119-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d119-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d119-132">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="7d119-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="7d119-133">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="7d119-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="7d119-134">**Свбемпривилежесет. Remove**</span><span class="sxs-lookup"><span data-stu-id="7d119-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




