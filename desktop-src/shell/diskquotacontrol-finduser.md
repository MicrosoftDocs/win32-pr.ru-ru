---
description: Поиск записи пользователя по имени в файле квоты тома.
title: Дисккуотаконтрол. Финдусер, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984253"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="39afb-103">Дисккуотаконтрол. Финдусер, метод</span><span class="sxs-lookup"><span data-stu-id="39afb-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="39afb-104">Поиск записи пользователя по имени в файле квоты тома.</span><span class="sxs-lookup"><span data-stu-id="39afb-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="39afb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39afb-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="39afb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39afb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39afb-107">*слогоннаме*</span><span class="sxs-lookup"><span data-stu-id="39afb-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="39afb-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="39afb-108">Type: **String**</span></span>

<span data-ttu-id="39afb-109">Строковое значение, содержащее имя входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="39afb-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39afb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39afb-110">Return value</span></span>

<span data-ttu-id="39afb-111">Возвращает выражение объекта, результатом которого является объект пользователя [**дидисккуотаусер**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="39afb-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39afb-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="39afb-112">Remarks</span></span>

<span data-ttu-id="39afb-113">Этот метод возвращает объект [**дидисккуотаусер**](didiskquotauser-object.md) , даже если в файле квоты нет записи для пользователя.</span><span class="sxs-lookup"><span data-stu-id="39afb-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="39afb-114">Возвращенный объект пользователя имеет порог предупреждения, а ограничения жестких квот установлены на значения по умолчанию для тома.</span><span class="sxs-lookup"><span data-stu-id="39afb-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="39afb-115">Строка, возвращаемая из [**транслателогоннаметосид**](diskquotacontrol-translatelogonnametosid.md) , может передаваться вместо параметра *слогоннаме* .</span><span class="sxs-lookup"><span data-stu-id="39afb-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="39afb-116">Когда **финдусер** получает строку идентификатора безопасности, она использует соответствующий идентификатор безопасности для прямого поиска записи квот пользователя на томе.</span><span class="sxs-lookup"><span data-stu-id="39afb-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="39afb-117">Это обходит кэш имен SID.</span><span class="sxs-lookup"><span data-stu-id="39afb-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="39afb-118">В случаях, когда **финдусер** завершается сбоем из-за несоответствия в формате (например, с SAM-совместимым и UPN) имени входа и кэшированного имени входа, имя входа может быть преобразовано в строку идентификатора SID с помощью **транслателогоннаметосид** , затем снова передается в **финдусер**.</span><span class="sxs-lookup"><span data-stu-id="39afb-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="39afb-119">Этот метод показан в следующем коде VBScript.</span><span class="sxs-lookup"><span data-stu-id="39afb-119">The following VBScript code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



## <a name="requirements"></a><span data-ttu-id="39afb-120">Требования</span><span class="sxs-lookup"><span data-stu-id="39afb-120">Requirements</span></span>



| <span data-ttu-id="39afb-121">Требование</span><span class="sxs-lookup"><span data-stu-id="39afb-121">Requirement</span></span> | <span data-ttu-id="39afb-122">Значение</span><span class="sxs-lookup"><span data-stu-id="39afb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39afb-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39afb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39afb-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39afb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39afb-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39afb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39afb-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39afb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="39afb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="39afb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39afb-128"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="39afb-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39afb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39afb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39afb-130">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="39afb-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




