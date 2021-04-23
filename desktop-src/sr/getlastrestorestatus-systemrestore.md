---
title: Метод Жетластресторестатус класса SystemRestore
description: Возвращает состояние последнего восстановления системы.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Восстановление системы метода Жетластресторестатус
- Восстановление системы метода Жетластресторестатус, класс SystemRestore
- Восстановление системы класса SystemRestore, метод Жетластресторестатус
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701021"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="00b2e-106">Метод Жетластресторестатус класса SystemRestore</span><span class="sxs-lookup"><span data-stu-id="00b2e-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="00b2e-107">Возвращает состояние последнего восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="00b2e-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b2e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00b2e-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="00b2e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="00b2e-109">Parameters</span></span>

<span data-ttu-id="00b2e-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="00b2e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00b2e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00b2e-111">Return value</span></span>

<span data-ttu-id="00b2e-112">Метод возвращает одно из следующих значений состояния.</span><span class="sxs-lookup"><span data-stu-id="00b2e-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="00b2e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00b2e-113">Return value</span></span>                                                                 | <span data-ttu-id="00b2e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="00b2e-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="00b2e-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="00b2e-116">Последнее восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="00b2e-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="00b2e-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="00b2e-118">Последнее восстановление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="00b2e-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="00b2e-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="00b2e-120">Последнее восстановление было прервано.</span><span class="sxs-lookup"><span data-stu-id="00b2e-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="00b2e-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="00b2e-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="00b2e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="00b2e-122">Requirements</span></span>



| <span data-ttu-id="00b2e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="00b2e-123">Requirement</span></span> | <span data-ttu-id="00b2e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="00b2e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="00b2e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00b2e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="00b2e-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="00b2e-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="00b2e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00b2e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="00b2e-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="00b2e-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="00b2e-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="00b2e-129">Namespace</span></span><br/>                | <span data-ttu-id="00b2e-130">Корневой каталог \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="00b2e-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="00b2e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="00b2e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00b2e-132"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00b2e-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00b2e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00b2e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b2e-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="00b2e-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





