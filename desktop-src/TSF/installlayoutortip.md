---
title: Функция Инсталллайаутортип
description: Включает указанные раскладки клавиатуры или текстовые службы.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- Платформа текстовых служб Инсталллайаутортип Function
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681898"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="71c21-104">Функция Инсталллайаутортип</span><span class="sxs-lookup"><span data-stu-id="71c21-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="71c21-105">Включает указанные раскладки клавиатуры или текстовые службы.</span><span class="sxs-lookup"><span data-stu-id="71c21-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71c21-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="71c21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71c21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c21-108">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71c21-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c21-109">Строка, представляющая список раскладок клавиатуры или профиль служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="71c21-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="71c21-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71c21-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71c21-111">Битовое значение, задающее следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="71c21-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="71c21-112">Следующие идентификаторы не определены в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="71c21-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="71c21-113">Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="71c21-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="71c21-114">Например, чтобы использовать **\_ Удаление илот** , необходимо включить `#define ILOT_UNINSTALL 0x00000001` в код.</span><span class="sxs-lookup"><span data-stu-id="71c21-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="71c21-115">Значение</span><span class="sxs-lookup"><span data-stu-id="71c21-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="71c21-116">Значение</span><span class="sxs-lookup"><span data-stu-id="71c21-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="71c21-117"><dt>**Илот \_ Удаление**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="71c21-118">То же, что и **илот \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="71c21-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="71c21-119"><dt>**Илот \_ ДЕФПРОФИЛЕ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="71c21-120">Задает указанный макет или Совет в качестве элемента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c21-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="71c21-121"><dt>**Илот \_ DEFUSER4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="71c21-122">Изменяет параметр. Параметры.</span><span class="sxs-lookup"><span data-stu-id="71c21-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="71c21-123"><dt>**Илот \_ СИСЛОКАЛЕ**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="71c21-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="71c21-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="71c21-125"><dt>**Илот \_ НОЛОКАЛЕТОЕНУМЕРАТЕ**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="71c21-126">Не используется.</span><span class="sxs-lookup"><span data-stu-id="71c21-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="71c21-127"><dt>**Илот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="71c21-128">Параметр сохраняется, но не применяется к текущему сеансу.</span><span class="sxs-lookup"><span data-stu-id="71c21-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="71c21-129"><dt>**Илот \_ КЛЕАНИНСТАЛЛ**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="71c21-130">Отключает все текущие раскладки клавиатуры и текстовые службы.</span><span class="sxs-lookup"><span data-stu-id="71c21-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="71c21-131"><dt>**Илот \_ ОТКЛЮЧЕНные**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="71c21-132">Отключает указанную раскладку клавиатуры и службу текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="71c21-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c21-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71c21-133">Return value</span></span>



| <span data-ttu-id="71c21-134">Код возврата</span><span class="sxs-lookup"><span data-stu-id="71c21-134">Return code</span></span>                                                                          | <span data-ttu-id="71c21-135">Описание</span><span class="sxs-lookup"><span data-stu-id="71c21-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="71c21-136"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="71c21-137">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="71c21-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="71c21-138"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="71c21-139">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="71c21-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71c21-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71c21-140">Remarks</span></span>

<span data-ttu-id="71c21-141">Формат строки в списке макета:</span><span class="sxs-lookup"><span data-stu-id="71c21-141">The string format of the layout list is:</span></span>

<span data-ttu-id="71c21-142"><LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="71c21-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="71c21-143">Формат строки в списке профиля службы текстового ввода:</span><span class="sxs-lookup"><span data-stu-id="71c21-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="71c21-144"><LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="71c21-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="71c21-145">Ниже приведен пример значения для параметра *ПСЗ* .</span><span class="sxs-lookup"><span data-stu-id="71c21-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="71c21-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="71c21-146">Examples</span></span>

<span data-ttu-id="71c21-147">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="71c21-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="71c21-148">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="71c21-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="71c21-149">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="71c21-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="71c21-150">Требования</span><span class="sxs-lookup"><span data-stu-id="71c21-150">Requirements</span></span>



| <span data-ttu-id="71c21-151">Требование</span><span class="sxs-lookup"><span data-stu-id="71c21-151">Requirement</span></span> | <span data-ttu-id="71c21-152">Значение</span><span class="sxs-lookup"><span data-stu-id="71c21-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71c21-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71c21-153">Minimum supported client</span></span><br/> | <span data-ttu-id="71c21-154">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71c21-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="71c21-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71c21-155">Minimum supported server</span></span><br/> | <span data-ttu-id="71c21-156">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71c21-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="71c21-157">DLL</span><span class="sxs-lookup"><span data-stu-id="71c21-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c21-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71c21-158"><dt>Input.dll</dt></span></span> </dl> |



 

