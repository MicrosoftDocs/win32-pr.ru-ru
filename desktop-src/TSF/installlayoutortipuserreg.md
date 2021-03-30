---
title: Функция Инсталллайаутортипусеррег
description: Включает указанные раскладки клавиатуры или текстовые службы для указанного пользователя.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Платформа текстовых служб Инсталллайаутортипусеррег Function
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802369"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="58a68-104">Функция Инсталллайаутортипусеррег</span><span class="sxs-lookup"><span data-stu-id="58a68-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="58a68-105">Включает указанные раскладки клавиатуры или текстовые службы для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="58a68-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a68-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58a68-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="58a68-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="58a68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a68-108">*псзусеррег* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="58a68-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58a68-109">Путь к реестру пользователя.</span><span class="sxs-lookup"><span data-stu-id="58a68-109">The registry path of the user.</span></span> <span data-ttu-id="58a68-110">Если этот параметр имеет **значение NULL**, \_ \_ используется текущий пользователь hKey.</span><span class="sxs-lookup"><span data-stu-id="58a68-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="58a68-111">*псзсистемрег* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="58a68-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58a68-112">Путь реестра системы.</span><span class="sxs-lookup"><span data-stu-id="58a68-112">The registry path of the system.</span></span> <span data-ttu-id="58a68-113">Если этот параметр имеет **значение NULL**, \_ \_ используется система локального компьютера hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="58a68-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="58a68-114">*псзсофтваререг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="58a68-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58a68-115">Путь реестра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="58a68-115">The registry path of the software.</span></span> <span data-ttu-id="58a68-116">Если этот параметр имеет **значение NULL**, \_ \_ \\ используется программное обеспечение для локального компьютера hKey.</span><span class="sxs-lookup"><span data-stu-id="58a68-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="58a68-117">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58a68-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a68-118">Строка, представляющая список раскладок клавиатуры или профиль служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="58a68-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="58a68-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58a68-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a68-120">Битовое значение, задающее следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="58a68-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="58a68-121">Следующие идентификаторы не определены в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="58a68-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="58a68-122">Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="58a68-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="58a68-123">Например, чтобы использовать **\_ Удаление илот** , необходимо включить `#define ILOT_UNINSTALL 0x00000001` в код.</span><span class="sxs-lookup"><span data-stu-id="58a68-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="58a68-124">Значение</span><span class="sxs-lookup"><span data-stu-id="58a68-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="58a68-125">Значение</span><span class="sxs-lookup"><span data-stu-id="58a68-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="58a68-126"><dt>**Илот \_ Удаление**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="58a68-127">То же, что и **илот \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="58a68-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="58a68-128"><dt>**Илот \_ ДЕФПРОФИЛЕ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="58a68-129">Задает указанный макет или Совет в качестве элемента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58a68-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="58a68-130"><dt>**Илот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="58a68-131">Параметр сохраняется, но не применяется к текущему сеансу.</span><span class="sxs-lookup"><span data-stu-id="58a68-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="58a68-132"><dt>**Илот \_ КЛЕАНИНСТАЛЛ**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="58a68-133">Отключает все текущие раскладки клавиатуры и текстовые службы.</span><span class="sxs-lookup"><span data-stu-id="58a68-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="58a68-134"><dt>**Илот \_ ОТКЛЮЧЕНные**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="58a68-135">Отключает указанную раскладку клавиатуры и службу текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="58a68-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a68-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58a68-136">Return value</span></span>



| <span data-ttu-id="58a68-137">Код возврата</span><span class="sxs-lookup"><span data-stu-id="58a68-137">Return code</span></span>                                                                         | <span data-ttu-id="58a68-138">Описание</span><span class="sxs-lookup"><span data-stu-id="58a68-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="58a68-139"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="58a68-140">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="58a68-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="58a68-141"><dt>**фасе**</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="58a68-142">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="58a68-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58a68-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58a68-143">Remarks</span></span>

<span data-ttu-id="58a68-144">Формат строки в списке макета:</span><span class="sxs-lookup"><span data-stu-id="58a68-144">The string format of the layout list is:</span></span>

<span data-ttu-id="58a68-145"><LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="58a68-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="58a68-146">Формат строки в списке профиля службы текстового ввода:</span><span class="sxs-lookup"><span data-stu-id="58a68-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="58a68-147"><LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="58a68-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="58a68-148">Ниже приведен пример значения для параметра *ПСЗ* .</span><span class="sxs-lookup"><span data-stu-id="58a68-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="58a68-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="58a68-149">Examples</span></span>

<span data-ttu-id="58a68-150">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="58a68-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="58a68-151">В следующем примере показано, как получить указатель на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="58a68-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="58a68-152">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="58a68-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="58a68-153">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="58a68-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="58a68-154">Требования</span><span class="sxs-lookup"><span data-stu-id="58a68-154">Requirements</span></span>



| <span data-ttu-id="58a68-155">Требование</span><span class="sxs-lookup"><span data-stu-id="58a68-155">Requirement</span></span> | <span data-ttu-id="58a68-156">Значение</span><span class="sxs-lookup"><span data-stu-id="58a68-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="58a68-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58a68-157">Minimum supported client</span></span><br/> | <span data-ttu-id="58a68-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58a68-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="58a68-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58a68-159">Minimum supported server</span></span><br/> | <span data-ttu-id="58a68-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58a68-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="58a68-161">DLL</span><span class="sxs-lookup"><span data-stu-id="58a68-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58a68-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58a68-162"><dt>Input.dll</dt></span></span> </dl> |



 

