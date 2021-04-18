---
title: Метод Креатересторепоинт класса SystemRestore
description: Создает точку восстановления.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Восстановление системы метода Креатересторепоинт
- Восстановление системы метода Креатересторепоинт, класс SystemRestore
- Восстановление системы класса SystemRestore, метод Креатересторепоинт
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491037"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="43970-106">Метод Креатересторепоинт класса SystemRestore</span><span class="sxs-lookup"><span data-stu-id="43970-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="43970-107">Создает точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-107">Creates a restore point.</span></span>

<span data-ttu-id="43970-108">Этот метод является эквивалентом функции [**срсетресторепоинт**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) с помощью скрипта.</span><span class="sxs-lookup"><span data-stu-id="43970-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="43970-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43970-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="43970-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="43970-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43970-111">*Описание* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43970-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43970-112">Отображаемое описание, чтобы пользователь мог легко найти точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="43970-113">Максимальная длина строки ANSI — MAX \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="43970-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="43970-114">Максимальная длина строки Юникода — MAX \_ DESC \_ W.</span><span class="sxs-lookup"><span data-stu-id="43970-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="43970-115">Дополнительные сведения см. в разделе [текст описания точки восстановления](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="43970-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="43970-116">*Ресторепоинттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43970-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43970-117">Тип точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-117">The type of restore point.</span></span> <span data-ttu-id="43970-118">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="43970-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="43970-119">Тип точки восстановления</span><span class="sxs-lookup"><span data-stu-id="43970-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="43970-120">Значение</span><span class="sxs-lookup"><span data-stu-id="43970-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="43970-121"><dt>**Приложение \_ УСТАНОВИТЬ**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43970-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="43970-122">Приложение установлено.</span><span class="sxs-lookup"><span data-stu-id="43970-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="43970-123"><dt>**Приложение \_ Удаление**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="43970-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="43970-124">Удалено приложение.</span><span class="sxs-lookup"><span data-stu-id="43970-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="43970-125"><dt>**Устройство \_ \_Установка драйвера**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="43970-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="43970-126">Установлен драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="43970-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="43970-127"><dt>**Изменение \_ Параметры**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="43970-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="43970-128">В приложении были добавлены или удалены компоненты.</span><span class="sxs-lookup"><span data-stu-id="43970-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="43970-129"><dt>**Отменено \_ Операция**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="43970-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="43970-130">Приложению необходимо удалить созданную точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="43970-131">Например, приложение будет использовать этот флаг, когда пользователь отменит установку.</span><span class="sxs-lookup"><span data-stu-id="43970-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="43970-132">*Тип события* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43970-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43970-133">Тип события.</span><span class="sxs-lookup"><span data-stu-id="43970-133">The type of event.</span></span> <span data-ttu-id="43970-134">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="43970-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="43970-135">Тип события</span><span class="sxs-lookup"><span data-stu-id="43970-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="43970-136">Значение</span><span class="sxs-lookup"><span data-stu-id="43970-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="43970-137"><dt>**Начало \_ ВЛОЖЕНное \_ \_ изменение системы**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="43970-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="43970-138">Начато изменение системы.</span><span class="sxs-lookup"><span data-stu-id="43970-138">A system change has begun.</span></span> <span data-ttu-id="43970-139">Последующий вложенный вызов не создает новую точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="43970-140">Последующие вызовы должны использовать КОНЕЧные \_ вложенные \_ \_ изменения системы, а не конечные \_ \_ изменения системы.</span><span class="sxs-lookup"><span data-stu-id="43970-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="43970-141"><dt>**Начало \_ \_Изменение системы**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="43970-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="43970-142">Начато изменение системы.</span><span class="sxs-lookup"><span data-stu-id="43970-142">A system change has begun.</span></span> <br/> <span data-ttu-id="43970-143">При последующем вызове должно использоваться КОНЕЧНОе \_ \_ изменение системы, а не незавершенное \_ вложенное \_ \_ изменение системы.</span><span class="sxs-lookup"><span data-stu-id="43970-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="43970-144"><dt>**Конец \_ ВЛОЖЕНное \_ \_ изменение системы**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="43970-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="43970-145">Изменение системы завершено.</span><span class="sxs-lookup"><span data-stu-id="43970-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="43970-146"><dt>**Конец \_ \_Изменение системы**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="43970-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="43970-147">Изменение системы завершено.</span><span class="sxs-lookup"><span data-stu-id="43970-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43970-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43970-148">Return value</span></span>

<span data-ttu-id="43970-149">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="43970-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="43970-150">В противном случае метод возвращает один из кодов ошибок COM, определенных в файле WinError. h.</span><span class="sxs-lookup"><span data-stu-id="43970-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="43970-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43970-151">Remarks</span></span>

<span data-ttu-id="43970-152">\* \* Windows 8: \* \*</span><span class="sxs-lookup"><span data-stu-id="43970-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="43970-153">Новый раздел реестра позволяет разработчикам приложений изменять частоту создания точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="43970-154">Приложения должны создать этот ключ, чтобы использовать его, так как он не будет существовать в системе.</span><span class="sxs-lookup"><span data-stu-id="43970-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="43970-155">Если ключ не существует, по умолчанию будет применено следующее.</span><span class="sxs-lookup"><span data-stu-id="43970-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="43970-156">Если приложение вызывает метод **креатересторепоинт** для создания точки восстановления, Windows пропускает создание этой новой точки восстановления, если в течение последних 24 часов были созданы какие-либо точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="43970-157">Метод **креатересторепоинт** возвращает значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="43970-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="43970-158">Разработчики могут создавать приложения, которые создают  значение DWORD **системресторепоинткреатионфрекуенци** в разделе реестра **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**.</span><span class="sxs-lookup"><span data-stu-id="43970-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="43970-159">Значение этого раздела реестра может изменить частоту создания точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="43970-160">Значение этого раздела реестра может изменить частоту создания точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="43970-161">Если приложение вызывает **креатересторепоинт** для создания точки восстановления, а значение раздела реестра равно 0, восстановление системы не пропускает создание новой точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="43970-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="43970-162">Если приложение вызывает **креатересторепоинт** для создания точки восстановления, а значение раздела реестра — целое число N, восстановление системы пропускает создание новой точки восстановления, если какие-либо точки восстановления были созданы в течение предыдущих N минут.</span><span class="sxs-lookup"><span data-stu-id="43970-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="43970-163">Примеры</span><span class="sxs-lookup"><span data-stu-id="43970-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="43970-164">Требования</span><span class="sxs-lookup"><span data-stu-id="43970-164">Requirements</span></span>



| <span data-ttu-id="43970-165">Требование</span><span class="sxs-lookup"><span data-stu-id="43970-165">Requirement</span></span> | <span data-ttu-id="43970-166">Значение</span><span class="sxs-lookup"><span data-stu-id="43970-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="43970-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43970-167">Minimum supported client</span></span><br/> | <span data-ttu-id="43970-168">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43970-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="43970-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43970-169">Minimum supported server</span></span><br/> | <span data-ttu-id="43970-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="43970-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="43970-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43970-171">Namespace</span></span><br/>                | <span data-ttu-id="43970-172">Корневой каталог \\ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="43970-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="43970-173">MOF</span><span class="sxs-lookup"><span data-stu-id="43970-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43970-174"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43970-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43970-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43970-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43970-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="43970-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





