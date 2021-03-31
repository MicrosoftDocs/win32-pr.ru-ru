---
title: Метод Restore класса SystemRestore
description: Инициирует восстановление системы.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Восстановление системы метода восстановления
- Восстановление системы метода Restore, класс SystemRestore
- SystemRestore класс System Restore, метод Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801384"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="86620-106">Метод Restore класса SystemRestore</span><span class="sxs-lookup"><span data-stu-id="86620-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="86620-107">Инициирует восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="86620-107">Initiates a system restore.</span></span> <span data-ttu-id="86620-108">Вызывающий объект должен принудительно выполнить перезагрузку системы.</span><span class="sxs-lookup"><span data-stu-id="86620-108">The caller must force a system reboot.</span></span> <span data-ttu-id="86620-109">Фактическое восстановление происходит во время перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="86620-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="86620-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86620-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="86620-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="86620-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86620-112">*SequenceNumber* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="86620-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86620-113">Порядковый номер точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="86620-113">The sequence number of the restore point.</span></span> <span data-ttu-id="86620-114">Чтобы определить порядковый номер для определенной точки восстановления, перечислите все точки восстановления в системе.</span><span class="sxs-lookup"><span data-stu-id="86620-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86620-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86620-115">Return value</span></span>

<span data-ttu-id="86620-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="86620-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="86620-117">В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.</span><span class="sxs-lookup"><span data-stu-id="86620-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="86620-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="86620-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="86620-119">Требования</span><span class="sxs-lookup"><span data-stu-id="86620-119">Requirements</span></span>



| <span data-ttu-id="86620-120">Требование</span><span class="sxs-lookup"><span data-stu-id="86620-120">Requirement</span></span> | <span data-ttu-id="86620-121">Значение</span><span class="sxs-lookup"><span data-stu-id="86620-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="86620-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86620-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86620-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="86620-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="86620-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86620-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86620-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86620-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="86620-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="86620-126">Namespace</span></span><br/>                | <span data-ttu-id="86620-127">Корневой каталог \\ \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="86620-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="86620-128">MOF</span><span class="sxs-lookup"><span data-stu-id="86620-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86620-129"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86620-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86620-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86620-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86620-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="86620-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





