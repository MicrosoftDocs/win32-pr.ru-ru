---
description: Преобразует имя входа в соответствующий идентификатор безопасности пользователя в строковом формате.
title: Дисккуотаконтрол. Транслателогоннаметосид, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081099"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="a585c-103">Дисккуотаконтрол. Транслателогоннаметосид, метод</span><span class="sxs-lookup"><span data-stu-id="a585c-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="a585c-104">Преобразует имя входа в соответствующий идентификатор безопасности пользователя в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="a585c-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="a585c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a585c-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="a585c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a585c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a585c-107">*логоннаме*</span><span class="sxs-lookup"><span data-stu-id="a585c-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="a585c-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="a585c-108">Type: **String**</span></span>

<span data-ttu-id="a585c-109">Строковое значение, указывающее имя пользователя для входа.</span><span class="sxs-lookup"><span data-stu-id="a585c-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a585c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a585c-110">Return value</span></span>

<span data-ttu-id="a585c-111">Возвращает идентификатор безопасности пользователя (SID) в строковом формате, соответствующий указанному имени входа.</span><span class="sxs-lookup"><span data-stu-id="a585c-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="a585c-112">Возвращаемая строка включает стандартные заключенные в фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="a585c-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="a585c-113">Например:</span><span class="sxs-lookup"><span data-stu-id="a585c-113">For example:</span></span>

<span data-ttu-id="a585c-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="a585c-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="a585c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a585c-115">Remarks</span></span>

<span data-ttu-id="a585c-116">Возвращенная строка идентификатора безопасности может быть передана в метод [**финдусер**](diskquotacontrol-finduser.md) вместо имени для входа.</span><span class="sxs-lookup"><span data-stu-id="a585c-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="a585c-117">При сбое вызова метода [**финдусер**](diskquotacontrol-finduser.md)( *логоннаме*) это может быть вызвано несоответствием между формой (например, совместимым с Security Account Manager \[ SAM \] и именем участника \[ -пользователя UPN \] ) имени входа и формы, хранящейся в кэше имен SID.</span><span class="sxs-lookup"><span data-stu-id="a585c-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="a585c-118">В таких случаях имя входа может быть преобразовано в идентификатор безопасности, а вызов **финдусер** повторяется.</span><span class="sxs-lookup"><span data-stu-id="a585c-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="a585c-119">**Финдусер** распознает строку идентификатора безопасности и обходит Поиск в КЭШЕ имен SID.</span><span class="sxs-lookup"><span data-stu-id="a585c-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="a585c-120">Этот прием показан на следующем коде VBScript (Microsoft Visual Basic Scripting Edition).</span><span class="sxs-lookup"><span data-stu-id="a585c-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


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



<span data-ttu-id="a585c-121">При сравнении уточняющих запросов в кэше имен SID процесс преобразования имени в идентификатор SID может оказаться очень длительным.</span><span class="sxs-lookup"><span data-stu-id="a585c-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="a585c-122">Таким образом, рекомендуется сначала вызвать [**финдусер**](diskquotacontrol-finduser.md) с именем для входа.</span><span class="sxs-lookup"><span data-stu-id="a585c-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="a585c-123">В приведенном выше примере используется этот метод.</span><span class="sxs-lookup"><span data-stu-id="a585c-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="a585c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a585c-124">Requirements</span></span>



| <span data-ttu-id="a585c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a585c-125">Requirement</span></span> | <span data-ttu-id="a585c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a585c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a585c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a585c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a585c-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a585c-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a585c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a585c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a585c-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a585c-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a585c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a585c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a585c-132"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a585c-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a585c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a585c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a585c-134">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="a585c-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




