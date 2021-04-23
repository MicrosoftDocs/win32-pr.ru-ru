---
title: Метод Disable класса SystemRestore
description: Отключает мониторинг на определенном диске.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Отключить восстановление системы метода
- Отключение метода Restore системы, класс SystemRestore
- SystemRestore класс System Restore, метод Disable
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136154"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="1e7a9-106">Метод Disable класса SystemRestore</span><span class="sxs-lookup"><span data-stu-id="1e7a9-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="1e7a9-107">Отключает мониторинг на определенном диске.</span><span class="sxs-lookup"><span data-stu-id="1e7a9-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e7a9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e7a9-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="1e7a9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e7a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e7a9-110">*Диск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7a9-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7a9-111">Диск, который должен быть отключен.</span><span class="sxs-lookup"><span data-stu-id="1e7a9-111">The drive to be disabled.</span></span> <span data-ttu-id="1e7a9-112">Строка диска должна иметь формат "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="1e7a9-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="1e7a9-113">Если этот параметр является системным диском или пустой строкой (""), диски не отслеживаются.</span><span class="sxs-lookup"><span data-stu-id="1e7a9-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e7a9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e7a9-114">Return value</span></span>

<span data-ttu-id="1e7a9-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1e7a9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1e7a9-116">В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.</span><span class="sxs-lookup"><span data-stu-id="1e7a9-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="1e7a9-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e7a9-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="1e7a9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1e7a9-118">Requirements</span></span>



| <span data-ttu-id="1e7a9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1e7a9-119">Requirement</span></span> | <span data-ttu-id="1e7a9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1e7a9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1e7a9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e7a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7a9-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1e7a9-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1e7a9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e7a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7a9-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e7a9-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="1e7a9-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1e7a9-125">Namespace</span></span><br/>                | <span data-ttu-id="1e7a9-126">Корневой каталог \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e7a9-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="1e7a9-127">MOF</span><span class="sxs-lookup"><span data-stu-id="1e7a9-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e7a9-128"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e7a9-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e7a9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e7a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e7a9-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="1e7a9-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





