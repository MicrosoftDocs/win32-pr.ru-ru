---
description: Создает указанный раздел реестра в автономном кусте реестра. Если ключ уже существует, функция открывает его.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Функция Оркреатекэй (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669159"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="dfa5f-104">Функция Оркреатекэй</span><span class="sxs-lookup"><span data-stu-id="dfa5f-104">ORCreateKey function</span></span>

<span data-ttu-id="dfa5f-105">Создает указанный раздел реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="dfa5f-106">Если ключ уже существует, функция открывает его.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa5f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfa5f-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="dfa5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfa5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa5f-109">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-110">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="dfa5f-111">*лпсубкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-112">Указатель на строку в Юникоде, содержащую имя подраздела, который открывается или создается этой функцией.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="dfa5f-113">Параметр *лпсубкэй* должен задавать подраздел ключа, определяемого параметром *Handle* . Он может иметь глубину до 32 уровней в дереве реестра.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="dfa5f-114">Дополнительные сведения о именах ключей см. [в разделе Структура реестра](../sysinfo/structure-of-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="dfa5f-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="dfa5f-115">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="dfa5f-116">Имена ключей не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="dfa5f-117">*лпкласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-118">Класс (тип объекта) этого ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-118">The class (object type) of this key.</span></span> <span data-ttu-id="dfa5f-119">Этот параметр можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-119">This parameter may be ignored.</span></span> <span data-ttu-id="dfa5f-120">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa5f-121">*двоптионс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-122">Этот параметр может иметь значение 0 или одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="dfa5f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa5f-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="dfa5f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa5f-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="dfa5f-125"><dt>**Reg \_ ПАРАМЕТР \_ Create \_ Link**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5f-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="dfa5f-126">Ключ является символьной ссылкой.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-126">The key is a symbolic link.</span></span> <span data-ttu-id="dfa5f-127">Целевой путь назначается значению L "Симболиклинквалуе" ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="dfa5f-128">Целевой путь должен быть абсолютным путем к реестру.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="dfa5f-129">Если этот параметр задан, также должен быть установлен **\_ параметр REG \_ без \_ постоянного режима** .</span><span class="sxs-lookup"><span data-stu-id="dfa5f-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="dfa5f-130">Если параметр *лпсубкэй* указывает существующий ключ, он должен быть создан с помощью **\_ команды реестра \_ Create \_ Link**.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="dfa5f-131">Символьные ссылки реестра следует использовать только в том случае, если это совершенно необходимо для совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="dfa5f-132"><dt>**Reg \_ \_ \_ Неизменяемый параметр "**</dt> <dt>0x00000000</dt> "</span><span class="sxs-lookup"><span data-stu-id="dfa5f-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="dfa5f-133">Ключ не является временным; Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="dfa5f-134">Информация хранится в файле и сохраняется при перезапуске системы.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="dfa5f-135">Функция [**орсавехиве**](orsavehive.md) сохраняет ключи, которые не являются временными.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="dfa5f-136">*псекуритидескриптор* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-137">Указатель на структуру [ \_ дескриптора безопасности](/windows/win32/api/winnt/ns-winnt-security_descriptor) , содержащую дескриптор безопасности для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="dfa5f-138">Если *псекуритидескриптор* имеет **значение NULL**, ключ получает дескриптор безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="dfa5f-139">Списки управления доступом в дескрипторе безопасности по умолчанию для ключа наследуются от его прямого родительского ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="dfa5f-140">*фкресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-141">Указатель на переменную, которая получает маркер для открытого или созданного ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="dfa5f-142">Используйте функцию [**орклосекэй**](orclosekey.md) , чтобы закрыть ключ после завершения использования маркера.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="dfa5f-143">*пдвдиспоситион* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="dfa5f-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5f-144">Указатель на переменную, которая получает одно из следующих значений метода обработки.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="dfa5f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa5f-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="dfa5f-146">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa5f-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="dfa5f-147"><dt>**Reg \_ СОЗДАН \_ новый \_ ключ**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5f-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="dfa5f-148">Ключ не существовал и был создан.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="dfa5f-149"><dt>**Reg \_ ОТКРЫТ \_ существующий \_ ключ**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5f-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="dfa5f-150">Ключ существовал и был просто открыт без изменения.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="dfa5f-151">Если *пдвдиспоситион* имеет **значение NULL**, сведения о расположении не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa5f-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfa5f-152">Return value</span></span>

<span data-ttu-id="dfa5f-153">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="dfa5f-154">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="dfa5f-155">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="dfa5f-156">Если параметр *двоптионс* установлен с параметром **реестра \_ \_ Create \_ Link** , но **\_ параметр REG \_ volatile имеет \_ неизменяемое** значение, или если возвращаемый маркер является обработчиком корневого ключа Hive, функция возвращает ошибку \_ Недопустимый \_ параметр.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa5f-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfa5f-157">Remarks</span></span>

<span data-ttu-id="dfa5f-158">Ключ, создаваемый функцией **оркреатекэй** , не имеет значений.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="dfa5f-159">Приложение может использовать функцию [**орсетвалуе**](orsetvalue.md) для установки значений ключей.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="dfa5f-160">Функцию **оркреатекэй** нельзя использовать для создания корневого ключа в кусте реестра вне сети.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="dfa5f-161">Используйте функцию [**оркреатехиве**](orcreatehive.md) для создания корневого ключа и получения маркера для ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="dfa5f-162">Автономный реестр не поддерживает сохранение отдельных ключей.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="dfa5f-163">Используйте функцию [**орсавехиве**](orsavehive.md) для сохранения ключа и его подразделов в кусте Hive.</span><span class="sxs-lookup"><span data-stu-id="dfa5f-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa5f-164">Требования</span><span class="sxs-lookup"><span data-stu-id="dfa5f-164">Requirements</span></span>



| <span data-ttu-id="dfa5f-165">Требование</span><span class="sxs-lookup"><span data-stu-id="dfa5f-165">Requirement</span></span> | <span data-ttu-id="dfa5f-166">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa5f-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa5f-167">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dfa5f-167">Redistributable</span></span><br/> | <span data-ttu-id="dfa5f-168">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="dfa5f-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="dfa5f-169">Header</span><span class="sxs-lookup"><span data-stu-id="dfa5f-169">Header</span></span><br/>          | <dl> <span data-ttu-id="dfa5f-170"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5f-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfa5f-171">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa5f-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="dfa5f-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5f-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa5f-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfa5f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa5f-174">**орклосекэй**</span><span class="sxs-lookup"><span data-stu-id="dfa5f-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="dfa5f-175">**оркреатехиве**</span><span class="sxs-lookup"><span data-stu-id="dfa5f-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="dfa5f-176">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="dfa5f-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="dfa5f-177">**орсавехиве**</span><span class="sxs-lookup"><span data-stu-id="dfa5f-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="dfa5f-178">\_дескриптор безопасности</span><span class="sxs-lookup"><span data-stu-id="dfa5f-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
