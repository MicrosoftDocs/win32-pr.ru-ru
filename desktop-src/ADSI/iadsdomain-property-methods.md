---
title: Методы свойств Иадсдомаин (iAds. h)
description: Методы интерфейса Иадсдомаин считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсдомаин ADSI
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989099"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="126e1-105">Методы свойств Иадсдомаин</span><span class="sxs-lookup"><span data-stu-id="126e1-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="126e1-106">Методы интерфейса [**иадсдомаин**](/windows/desktop/api/Iads/nn-iads-iadsdomain) считывают и записывают свойства, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="126e1-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="126e1-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="126e1-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="126e1-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="126e1-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="126e1-109">**аутаунлоккинтервал**</span><span class="sxs-lookup"><span data-stu-id="126e1-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="126e1-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-111">Указывает минимальное время, которое должно пройти до автоматического повторного включения учетной записи.</span><span class="sxs-lookup"><span data-stu-id="126e1-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="126e1-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-114">**Рабочая группа**</span><span class="sxs-lookup"><span data-stu-id="126e1-114">**IsWorkgroup**</span></span>
<span data-ttu-id="126e1-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-116">Это свойство больше не реализовано.</span><span class="sxs-lookup"><span data-stu-id="126e1-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="126e1-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="126e1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="126e1-118">Тип данных скрипта: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="126e1-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-119">**локкаутобсерватионинтервал**</span><span class="sxs-lookup"><span data-stu-id="126e1-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="126e1-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-121">Указывает временное окно, в течение которого отслеживается количество неудачных паролей и производится их сбор перед определением того, нужно ли заблокировать учетную запись. Например, если количество неудачных попыток ввода пароля для учетной записи превысит пороговое значение (максимально допустимое число недопустимых паролей) в течение указанного периода времени (интервал наблюдения за блокировкой), учетная запись будет заблокирована путем установки соответствующего свойства в наборе свойств параметров имени входа.</span><span class="sxs-lookup"><span data-stu-id="126e1-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="126e1-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-123">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-124">**максбадпассвордсалловед**</span><span class="sxs-lookup"><span data-stu-id="126e1-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="126e1-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-126">Указывает максимальное число недопустимых имен входа, разрешенных до блокировки учетной записи.</span><span class="sxs-lookup"><span data-stu-id="126e1-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="126e1-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-128">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-129">**макспассвордаже**</span><span class="sxs-lookup"><span data-stu-id="126e1-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="126e1-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-131">Указывает максимальный интервал времени в секундах, по истечении которого пароль должен быть изменен пользователем.</span><span class="sxs-lookup"><span data-stu-id="126e1-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="126e1-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-133">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-134">**минпассвордаже**</span><span class="sxs-lookup"><span data-stu-id="126e1-134">**MinPasswordAge**</span></span>
<span data-ttu-id="126e1-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-136">Указывает минимальный интервал времени в секундах, по истечении которого можно изменить пароль.</span><span class="sxs-lookup"><span data-stu-id="126e1-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="126e1-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-138">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-139">**минпассвордленгс**</span><span class="sxs-lookup"><span data-stu-id="126e1-139">**MinPasswordLength**</span></span>
<span data-ttu-id="126e1-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-141">Указывает минимальное число символов, которые должны использоваться для пароля.</span><span class="sxs-lookup"><span data-stu-id="126e1-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="126e1-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-143">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-144">**пассвордаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="126e1-144">**PasswordAttributes**</span></span>
<span data-ttu-id="126e1-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-146">Указывает ограничения на пароли, как определено в следующем списке атрибутов и значений.</span><span class="sxs-lookup"><span data-stu-id="126e1-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="126e1-147">Для \_ сложного атрибута attr пароль \_ должен включать по крайней мере один знак пунктуации или непечатный символ.</span><span class="sxs-lookup"><span data-stu-id="126e1-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="126e1-148">**Пароль \_ ATTR \_ None** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="126e1-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="126e1-149">**Пароль \_ ATTR, \_ смешанный \_ регистр** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="126e1-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="126e1-150">**Пароль \_ ATTR, \_ сложные** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="126e1-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="126e1-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-152">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="126e1-153">**пассвордхисториленгс**</span><span class="sxs-lookup"><span data-stu-id="126e1-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="126e1-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="126e1-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="126e1-155">Указывает число предыдущих паролей, сохраненных в списке журнала.</span><span class="sxs-lookup"><span data-stu-id="126e1-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="126e1-156">Пользователь не может повторно использовать пароль в списке журнала.</span><span class="sxs-lookup"><span data-stu-id="126e1-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="126e1-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="126e1-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="126e1-158">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="126e1-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="126e1-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="126e1-159">Examples</span></span>

<span data-ttu-id="126e1-160">В следующем примере кода выводится значение свойства **пассвордхисториленгс** .</span><span class="sxs-lookup"><span data-stu-id="126e1-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="126e1-161">В следующем примере кода выводится значение свойства **пассвордхисториленгс** .</span><span class="sxs-lookup"><span data-stu-id="126e1-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="126e1-162">Требования</span><span class="sxs-lookup"><span data-stu-id="126e1-162">Requirements</span></span>



| <span data-ttu-id="126e1-163">Требование</span><span class="sxs-lookup"><span data-stu-id="126e1-163">Requirement</span></span> | <span data-ttu-id="126e1-164">Значение</span><span class="sxs-lookup"><span data-stu-id="126e1-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="126e1-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="126e1-165">Minimum supported client</span></span><br/> | <span data-ttu-id="126e1-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="126e1-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="126e1-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="126e1-167">Minimum supported server</span></span><br/> | <span data-ttu-id="126e1-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="126e1-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="126e1-169">Header</span><span class="sxs-lookup"><span data-stu-id="126e1-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="126e1-170"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="126e1-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="126e1-171">DLL</span><span class="sxs-lookup"><span data-stu-id="126e1-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="126e1-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="126e1-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="126e1-173">IID</span><span class="sxs-lookup"><span data-stu-id="126e1-173">IID</span></span><br/>                      | <span data-ttu-id="126e1-174">IID \_ иадсдомаин определен как 00E4C220-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="126e1-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="126e1-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="126e1-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126e1-176">**иадсдомаин**</span><span class="sxs-lookup"><span data-stu-id="126e1-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="126e1-177">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="126e1-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





