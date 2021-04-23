---
title: Функция Куерилайаутортипстрингусеррег
description: Запрашивает указанную строку, которая представляет формат списка раскладки клавиатуры или профиля служб текстового ввода в указанном пути реестра.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Платформа текстовых служб Куерилайаутортипстрингусеррег Function
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682041"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="41729-104">Функция Куерилайаутортипстрингусеррег</span><span class="sxs-lookup"><span data-stu-id="41729-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="41729-105">Запрашивает указанную строку, которая представляет формат списка раскладки клавиатуры или профиля служб текстового ввода в указанном пути реестра.</span><span class="sxs-lookup"><span data-stu-id="41729-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="41729-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41729-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="41729-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="41729-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41729-108">*псзусеррег* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41729-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41729-109">Путь к реестру пользователя.</span><span class="sxs-lookup"><span data-stu-id="41729-109">The registry path of the user.</span></span> <span data-ttu-id="41729-110">Если этот параметр имеет **значение NULL**, \_ \_ используется текущий пользователь hKey.</span><span class="sxs-lookup"><span data-stu-id="41729-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="41729-111">*псзсистемрег* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41729-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41729-112">Путь реестра системы.</span><span class="sxs-lookup"><span data-stu-id="41729-112">The registry path of the system.</span></span> <span data-ttu-id="41729-113">Если этот параметр имеет **значение NULL**, \_ \_ используется система локального компьютера hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="41729-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="41729-114">*псзсофтваререг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41729-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41729-115">Путь реестра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="41729-115">The registry path of the software.</span></span> <span data-ttu-id="41729-116">Если этот параметр имеет **значение NULL**, \_ \_ \\ используется программное обеспечение для локального компьютера hKey.</span><span class="sxs-lookup"><span data-stu-id="41729-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="41729-117">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41729-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41729-118">Строка, представляющая раскладку клавиатуры или список профилей служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="41729-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="41729-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41729-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41729-120">Атрибут должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="41729-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41729-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41729-121">Return value</span></span>

<span data-ttu-id="41729-122">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="41729-122">This function can return one of these values.</span></span>



| <span data-ttu-id="41729-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="41729-123">Return code</span></span>                                                                                  | <span data-ttu-id="41729-124">Описание</span><span class="sxs-lookup"><span data-stu-id="41729-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="41729-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="41729-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="41729-126">Все макеты или профили, определенные в **ПСЗ** , являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="41729-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="41729-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="41729-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="41729-128">Один или несколько макетов или профилей, определенных в **ПСЗ** , являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="41729-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41729-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41729-129">Remarks</span></span>

<span data-ttu-id="41729-130">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="41729-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="41729-131">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="41729-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="41729-132">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="41729-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="41729-133">Формат строки в списке макета:</span><span class="sxs-lookup"><span data-stu-id="41729-133">The string format of the layout list is:</span></span>

<span data-ttu-id="41729-134"><LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="41729-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="41729-135">Формат строки в списке профиля службы текстового ввода:</span><span class="sxs-lookup"><span data-stu-id="41729-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="41729-136"><LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="41729-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="41729-137">Ниже приведен пример значения для параметра *ПСЗ* .</span><span class="sxs-lookup"><span data-stu-id="41729-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="41729-138">Требования</span><span class="sxs-lookup"><span data-stu-id="41729-138">Requirements</span></span>



| <span data-ttu-id="41729-139">Требование</span><span class="sxs-lookup"><span data-stu-id="41729-139">Requirement</span></span> | <span data-ttu-id="41729-140">Значение</span><span class="sxs-lookup"><span data-stu-id="41729-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41729-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41729-141">Minimum supported client</span></span><br/> | <span data-ttu-id="41729-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41729-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="41729-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41729-143">Minimum supported server</span></span><br/> | <span data-ttu-id="41729-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41729-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41729-145">DLL</span><span class="sxs-lookup"><span data-stu-id="41729-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41729-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41729-146"><dt>Input.dll</dt></span></span> </dl> |



 

