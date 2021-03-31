---
title: Функция Сетдефаултлайаутортип
description: Задает указанную раскладку клавиатуры или службу текстового ввода в качестве входного элемента по умолчанию для текущего пользователя.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Платформа текстовых служб Сетдефаултлайаутортип Function
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135427"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="08c01-104">Функция Сетдефаултлайаутортип</span><span class="sxs-lookup"><span data-stu-id="08c01-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="08c01-105">Задает указанную раскладку клавиатуры или службу текстового ввода в качестве входного элемента по умолчанию для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="08c01-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c01-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08c01-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="08c01-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c01-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c01-108">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08c01-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c01-109">Строка, представляющая раскладку клавиатуры или список профилей служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="08c01-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="08c01-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08c01-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c01-111">Битовое значение, задающее следующие флаги.</span><span class="sxs-lookup"><span data-stu-id="08c01-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="08c01-112">Следующие идентификаторы не определены в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="08c01-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="08c01-113">Необходимо либо использовать шестнадцатеричное значение, либо \# определить идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="08c01-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="08c01-114">Например, чтобы использовать СДЛОТ \_ ноапплитокуррентсессион, необходимо включить \# \_ в код определение сдлот ноапплитокуррентсессион 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="08c01-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="08c01-115">Значение</span><span class="sxs-lookup"><span data-stu-id="08c01-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="08c01-116">Значение</span><span class="sxs-lookup"><span data-stu-id="08c01-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="08c01-117"><dt>**Сдлот \_ НОАППЛИТОКУРРЕНТСЕССИОН**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="08c01-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="08c01-118">Сохраняет параметр в реестре, но четкое не обновляет параметр клавиатуры среды выполнения текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="08c01-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="08c01-119">Если альтернативный путь реестра задан в [**сетдефаултлайаутортипусеррег**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), этот флаг должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="08c01-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="08c01-120"><dt>**Сдлот \_ АППЛИТОКУРРЕНТСРЕАД**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="08c01-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="08c01-121">Применяет параметр сразу к текущему потоку.</span><span class="sxs-lookup"><span data-stu-id="08c01-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c01-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08c01-122">Return value</span></span>



| <span data-ttu-id="08c01-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="08c01-123">Return code</span></span>                                                                          | <span data-ttu-id="08c01-124">Описание</span><span class="sxs-lookup"><span data-stu-id="08c01-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="08c01-125"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="08c01-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="08c01-126">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="08c01-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="08c01-127"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="08c01-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="08c01-128">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="08c01-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08c01-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08c01-129">Remarks</span></span>

<span data-ttu-id="08c01-130">Формат строки в списке макета:</span><span class="sxs-lookup"><span data-stu-id="08c01-130">The string format of the layout list is:</span></span>

<span data-ttu-id="08c01-131"><LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="08c01-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="08c01-132">Формат строки в списке профиля службы текстового ввода:</span><span class="sxs-lookup"><span data-stu-id="08c01-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="08c01-133"><LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="08c01-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="08c01-134">Ниже приведен пример значения для параметра *ПСЗ* .</span><span class="sxs-lookup"><span data-stu-id="08c01-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="08c01-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="08c01-135">Examples</span></span>

<span data-ttu-id="08c01-136">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="08c01-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="08c01-137">В следующем примере показано, как получить указатель на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="08c01-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="08c01-138">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="08c01-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="08c01-139">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="08c01-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="08c01-140">Требования</span><span class="sxs-lookup"><span data-stu-id="08c01-140">Requirements</span></span>



| <span data-ttu-id="08c01-141">Требование</span><span class="sxs-lookup"><span data-stu-id="08c01-141">Requirement</span></span> | <span data-ttu-id="08c01-142">Значение</span><span class="sxs-lookup"><span data-stu-id="08c01-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08c01-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08c01-143">Minimum supported client</span></span><br/> | <span data-ttu-id="08c01-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08c01-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="08c01-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08c01-145">Minimum supported server</span></span><br/> | <span data-ttu-id="08c01-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08c01-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="08c01-147">DLL</span><span class="sxs-lookup"><span data-stu-id="08c01-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08c01-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08c01-148"><dt>Input.dll</dt></span></span> </dl> |



 

