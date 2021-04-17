---
title: Enable, метод класса SystemRestore
description: Включает наблюдение на определенном диске.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Включить восстановление системы метода
- Включить восстановление системы методов, класс SystemRestore
- SystemRestore класс System Restore, Enable, метод
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710503"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="860b4-106">Enable, метод класса SystemRestore</span><span class="sxs-lookup"><span data-stu-id="860b4-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="860b4-107">Включает наблюдение на определенном диске.</span><span class="sxs-lookup"><span data-stu-id="860b4-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="860b4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="860b4-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="860b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="860b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="860b4-110">*Диск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="860b4-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="860b4-111">Диск, который должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="860b4-111">The drive to be enabled.</span></span> <span data-ttu-id="860b4-112">Строка диска должна иметь формат "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="860b4-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="860b4-113">Если этот параметр является системным диском или пустой строкой (""), отслеживаются все диски.</span><span class="sxs-lookup"><span data-stu-id="860b4-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="860b4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="860b4-114">Return value</span></span>

<span data-ttu-id="860b4-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="860b4-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="860b4-116">В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.</span><span class="sxs-lookup"><span data-stu-id="860b4-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="860b4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="860b4-117">Remarks</span></span>

<span data-ttu-id="860b4-118">Метод **Enable** не ждет, пока наблюдение будет включено полностью перед возвратом, так как это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="860b4-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="860b4-119">Вместо этого он возвращается сразу после запуска службы восстановления системы и драйвера фильтра.</span><span class="sxs-lookup"><span data-stu-id="860b4-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="860b4-120">Чтобы включить восстановление системы на несистемном диске, необходимо сначала включить функцию восстановления системы на системном диске.</span><span class="sxs-lookup"><span data-stu-id="860b4-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="860b4-121">Этот метод завершает работу неудачно в режиме безопасного режима.</span><span class="sxs-lookup"><span data-stu-id="860b4-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="860b4-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="860b4-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="860b4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="860b4-123">Requirements</span></span>



| <span data-ttu-id="860b4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="860b4-124">Requirement</span></span> | <span data-ttu-id="860b4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="860b4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="860b4-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="860b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="860b4-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="860b4-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="860b4-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="860b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="860b4-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="860b4-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="860b4-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="860b4-130">Namespace</span></span><br/>                | <span data-ttu-id="860b4-131">Корневой каталог \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="860b4-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="860b4-132">MOF</span><span class="sxs-lookup"><span data-stu-id="860b4-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="860b4-133"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="860b4-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="860b4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="860b4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="860b4-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="860b4-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





