---
title: Функция Савесистемакктинпутсеттингс
description: Применяет параметр "Пользовательская раскладка клавиатуры и служба текстового ввода" к кусту "системные учетные записи".
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Платформа текстовых служб Савесистемакктинпутсеттингс Function
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414845"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="10684-104">Функция Савесистемакктинпутсеттингс</span><span class="sxs-lookup"><span data-stu-id="10684-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="10684-105">Применяет параметр "Пользовательская раскладка клавиатуры и служба текстового ввода" к кусту "системные учетные записи".</span><span class="sxs-lookup"><span data-stu-id="10684-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="10684-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10684-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="10684-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="10684-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10684-108">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10684-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10684-109">Родительское окно для диалогового окна "предупреждение".</span><span class="sxs-lookup"><span data-stu-id="10684-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="10684-110">Диалоговое окно предупреждение не всегда отображается и отображается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="10684-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="10684-111">Если этот параметр имеет **значение NULL**, диалоговое окно предупреждения отображаться не будет.</span><span class="sxs-lookup"><span data-stu-id="10684-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="10684-112">*хсаурцерегкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10684-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10684-113">Корневой раздел реестра для копируемого параметра пользователя.</span><span class="sxs-lookup"><span data-stu-id="10684-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10684-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10684-114">Return value</span></span>



| <span data-ttu-id="10684-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="10684-115">Return code</span></span>                                                                          | <span data-ttu-id="10684-116">Описание</span><span class="sxs-lookup"><span data-stu-id="10684-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="10684-117"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="10684-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="10684-118">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="10684-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="10684-119"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="10684-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="10684-120">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="10684-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10684-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10684-121">Remarks</span></span>

<span data-ttu-id="10684-122">Куст системной учетной записи — это \_ Пользователи hKey \\ . ПО УМОЛЧАНИю, HKEY \_ Users \\ s-1-5-19 и hKey \_ Users \\ s-1-5-20.</span><span class="sxs-lookup"><span data-stu-id="10684-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="10684-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="10684-123">Examples</span></span>

<span data-ttu-id="10684-124">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="10684-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="10684-125">В следующем примере показано, как получить указатель на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="10684-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="10684-126">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="10684-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="10684-127">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="10684-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="10684-128">Требования</span><span class="sxs-lookup"><span data-stu-id="10684-128">Requirements</span></span>



| <span data-ttu-id="10684-129">Требование</span><span class="sxs-lookup"><span data-stu-id="10684-129">Requirement</span></span> | <span data-ttu-id="10684-130">Значение</span><span class="sxs-lookup"><span data-stu-id="10684-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10684-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10684-131">Minimum supported client</span></span><br/> | <span data-ttu-id="10684-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10684-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="10684-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10684-133">Minimum supported server</span></span><br/> | <span data-ttu-id="10684-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10684-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10684-135">DLL</span><span class="sxs-lookup"><span data-stu-id="10684-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10684-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10684-136"><dt>Input.dll</dt></span></span> </dl> |



 

