---
description: Метод Remove объекта Свбемпривилежесет удаляет права доступа из коллекции.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Метод Свбемпривилежесет. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910276"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="31627-103">Свбемпривилежесет. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="31627-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="31627-104">Метод **Remove** объекта [**свбемпривилежесет**](swbemprivilegeset.md) удаляет права доступа из коллекции.</span><span class="sxs-lookup"><span data-stu-id="31627-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="31627-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="31627-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31627-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31627-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="31627-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="31627-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31627-108">*ипривилеже*</span><span class="sxs-lookup"><span data-stu-id="31627-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="31627-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="31627-109">Required.</span></span> <span data-ttu-id="31627-110">Это одна из констант WMI из группы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="31627-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="31627-111">Эти константы по сути представляют собой целые числа, представляющие определенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="31627-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="31627-112">Например, чтобы удалить привилегию, позволяющую завершить работу системы Windows, используйте константу **вбемпривилежешутдовн** или числовой эквивалент 0x17.</span><span class="sxs-lookup"><span data-stu-id="31627-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31627-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31627-113">Return value</span></span>

<span data-ttu-id="31627-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="31627-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31627-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="31627-115">Error codes</span></span>

<span data-ttu-id="31627-116">После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="31627-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="31627-117">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="31627-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="31627-118">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="31627-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="31627-119">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="31627-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="31627-120">Указанное право доступа не существует.</span><span class="sxs-lookup"><span data-stu-id="31627-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31627-121">Требования</span><span class="sxs-lookup"><span data-stu-id="31627-121">Requirements</span></span>



| <span data-ttu-id="31627-122">Требование</span><span class="sxs-lookup"><span data-stu-id="31627-122">Requirement</span></span> | <span data-ttu-id="31627-123">Значение</span><span class="sxs-lookup"><span data-stu-id="31627-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31627-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31627-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31627-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31627-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31627-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31627-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31627-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31627-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31627-128">Header</span><span class="sxs-lookup"><span data-stu-id="31627-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="31627-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31627-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="31627-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="31627-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="31627-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31627-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="31627-132">DLL</span><span class="sxs-lookup"><span data-stu-id="31627-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31627-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31627-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="31627-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="31627-134">CLSID</span></span><br/>                    | <span data-ttu-id="31627-135">\_СВБЕМПРИВИЛЕЖЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="31627-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="31627-136">IID</span><span class="sxs-lookup"><span data-stu-id="31627-136">IID</span></span><br/>                      | <span data-ttu-id="31627-137">IID \_ исвбемпривилежесет</span><span class="sxs-lookup"><span data-stu-id="31627-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="31627-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31627-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31627-139">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="31627-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="31627-140">**Свбемпривилежесет. Add**</span><span class="sxs-lookup"><span data-stu-id="31627-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




