---
title: Функция Сетдефаултлайаутортипусеррег
description: Задает указанную раскладку клавиатуры или текстовую службу в качестве входного элемента по умолчанию для пользовательского реестра.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Платформа текстовых служб Сетдефаултлайаутортипусеррег Function
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135251"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="98ec2-104">Функция Сетдефаултлайаутортипусеррег</span><span class="sxs-lookup"><span data-stu-id="98ec2-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="98ec2-105">Задает указанную раскладку клавиатуры или текстовую службу в качестве входного элемента по умолчанию для пользовательского реестра.</span><span class="sxs-lookup"><span data-stu-id="98ec2-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ec2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98ec2-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="98ec2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ec2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ec2-108">*псзусеррег* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98ec2-109">Путь к реестру пользователя.</span><span class="sxs-lookup"><span data-stu-id="98ec2-109">The registry path of the user.</span></span> <span data-ttu-id="98ec2-110">Если этот параметр имеет **значение NULL**, \_ \_ используется текущий пользователь hKey.</span><span class="sxs-lookup"><span data-stu-id="98ec2-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="98ec2-111">*псзсистемрег* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98ec2-112">Путь реестра системы.</span><span class="sxs-lookup"><span data-stu-id="98ec2-112">The registry path of the system.</span></span> <span data-ttu-id="98ec2-113">Если этот параметр имеет **значение NULL**, \_ \_ используется система локального компьютера hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="98ec2-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="98ec2-114">*псзсофтваререг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98ec2-115">Путь реестра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="98ec2-115">The registry path of the software.</span></span> <span data-ttu-id="98ec2-116">Если этот параметр имеет **значение NULL**, \_ \_ \\ используется программное обеспечение для локального компьютера hKey.</span><span class="sxs-lookup"><span data-stu-id="98ec2-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="98ec2-117">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98ec2-118">Строка, представляющая список раскладок клавиатуры или профиль служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="98ec2-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="98ec2-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98ec2-120">Битовое значение, задающее следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="98ec2-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="98ec2-121">Следующие идентификаторы не определены в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="98ec2-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="98ec2-122">Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="98ec2-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="98ec2-123">Например, чтобы использовать СДЛОТ \_ ноапплитокуррентсессион, необходимо включить \# \_ в код определение сдлот ноапплитокуррентсессион 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="98ec2-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="98ec2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="98ec2-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="98ec2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="98ec2-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="98ec2-126"><dt>**Сдлот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="98ec2-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="98ec2-127">Сохраняет параметр в реестре, но четкое не обновляет параметр клавиатуры среды выполнения текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="98ec2-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="98ec2-128">Если альтернативный путь реестра задан в **сетдефаултлайаутортипусеррег**, этот флаг должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="98ec2-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="98ec2-129"><dt>**Сдлот \_ АППЛИТОКУРРЕНТСРЕАД**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="98ec2-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="98ec2-130">Применяет параметр сразу к текущему потоку.</span><span class="sxs-lookup"><span data-stu-id="98ec2-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ec2-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98ec2-131">Return value</span></span>



| <span data-ttu-id="98ec2-132">Код возврата</span><span class="sxs-lookup"><span data-stu-id="98ec2-132">Return code</span></span>                                                                          | <span data-ttu-id="98ec2-133">Описание</span><span class="sxs-lookup"><span data-stu-id="98ec2-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="98ec2-134"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="98ec2-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="98ec2-135">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="98ec2-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="98ec2-136"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="98ec2-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="98ec2-137">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="98ec2-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98ec2-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98ec2-138">Remarks</span></span>

<span data-ttu-id="98ec2-139">Формат строки в списке макета:</span><span class="sxs-lookup"><span data-stu-id="98ec2-139">The string format of the layout list is:</span></span>

<span data-ttu-id="98ec2-140"><LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="98ec2-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="98ec2-141">Формат строки в списке профиля службы текстового ввода:</span><span class="sxs-lookup"><span data-stu-id="98ec2-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="98ec2-142"><LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="98ec2-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="98ec2-143">Ниже приведен пример значения для параметра *ПСЗ* .</span><span class="sxs-lookup"><span data-stu-id="98ec2-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="98ec2-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="98ec2-144">Examples</span></span>

<span data-ttu-id="98ec2-145">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="98ec2-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="98ec2-146">В следующем примере показано, как получить указатель на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="98ec2-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="98ec2-147">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="98ec2-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="98ec2-148">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="98ec2-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="98ec2-149">Требования</span><span class="sxs-lookup"><span data-stu-id="98ec2-149">Requirements</span></span>



| <span data-ttu-id="98ec2-150">Требование</span><span class="sxs-lookup"><span data-stu-id="98ec2-150">Requirement</span></span> | <span data-ttu-id="98ec2-151">Значение</span><span class="sxs-lookup"><span data-stu-id="98ec2-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="98ec2-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98ec2-152">Minimum supported client</span></span><br/> | <span data-ttu-id="98ec2-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="98ec2-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98ec2-154">Minimum supported server</span></span><br/> | <span data-ttu-id="98ec2-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98ec2-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="98ec2-156">DLL</span><span class="sxs-lookup"><span data-stu-id="98ec2-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ec2-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ec2-157"><dt>Input.dll</dt></span></span> </dl> |



 

