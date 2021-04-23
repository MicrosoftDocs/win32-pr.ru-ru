---
title: Функция Куерилайаутортипстринг
description: Запрашивает указанную строку, которая представляет формат списка раскладки клавиатуры или списка профилей служб текстового ввода.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Платформа текстовых служб Куерилайаутортипстринг Function
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682042"
---
# <a name="querylayoutortipstring-function"></a><span data-ttu-id="0eb8f-104">Функция Куерилайаутортипстринг</span><span class="sxs-lookup"><span data-stu-id="0eb8f-104">QueryLayoutOrTipString function</span></span>

<span data-ttu-id="0eb8f-105">Запрашивает указанную строку, которая представляет формат списка раскладки клавиатуры или списка профилей служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb8f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0eb8f-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0eb8f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0eb8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eb8f-108">*ПСЗ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0eb8f-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eb8f-109">Строка, представляющая раскладку клавиатуры или список профилей служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="0eb8f-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0eb8f-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eb8f-111">Атрибут должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-111">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eb8f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0eb8f-112">Return value</span></span>

<span data-ttu-id="0eb8f-113">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-113">This function can return one of these values.</span></span>



| <span data-ttu-id="0eb8f-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0eb8f-114">Return code</span></span>                                                                                  | <span data-ttu-id="0eb8f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0eb8f-115">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0eb8f-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0eb8f-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0eb8f-117">Все макеты или профили, определенные в *ПСЗ* , являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-117">All layouts or profiles defined in *psz* are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="0eb8f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0eb8f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0eb8f-119">Один или несколько макетов или профилей, определенных в *ПСЗ* , являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-119">One or more of the layouts or profiles defined in *psz* are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0eb8f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0eb8f-120">Remarks</span></span>

<span data-ttu-id="0eb8f-121">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0eb8f-121">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="0eb8f-122">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="0eb8f-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="0eb8f-123">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="0eb8f-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="0eb8f-124">Формат строки в списке макета:</span><span class="sxs-lookup"><span data-stu-id="0eb8f-124">The string format of the layout list is:</span></span>

<span data-ttu-id="0eb8f-125"><LangID 1>: <КЛИД 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="0eb8f-125"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="0eb8f-126">Формат строки в списке профиля службы текстового ввода:</span><span class="sxs-lookup"><span data-stu-id="0eb8f-126">The string format of the text service profile list is:</span></span>

<span data-ttu-id="0eb8f-127"><LangID 1>: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="0eb8f-127"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="0eb8f-128">Ниже приведен пример значения для параметра *ПСЗ* .</span><span class="sxs-lookup"><span data-stu-id="0eb8f-128">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="0eb8f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0eb8f-129">Requirements</span></span>



| <span data-ttu-id="0eb8f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0eb8f-130">Requirement</span></span> | <span data-ttu-id="0eb8f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0eb8f-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb8f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0eb8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb8f-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0eb8f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0eb8f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0eb8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb8f-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0eb8f-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0eb8f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0eb8f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0eb8f-137"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eb8f-137"><dt>Input.dll</dt></span></span> </dl> |



 

