---
title: Функция Саведефаултусеринпутсеттингс
description: Применяет параметр "Пользовательская раскладка клавиатуры" и "служба текстового ввода" к кусту пользователя по умолчанию.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- Платформа текстовых служб Саведефаултусеринпутсеттингс Function
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415109"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="a1a4d-104">Функция Саведефаултусеринпутсеттингс</span><span class="sxs-lookup"><span data-stu-id="a1a4d-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="a1a4d-105">Применяет параметр "Пользовательская раскладка клавиатуры" и "служба текстового ввода" к кусту пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a4d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1a4d-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="a1a4d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1a4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a4d-108">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1a4d-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a4d-109">Родительское окно для диалогового окна "предупреждение".</span><span class="sxs-lookup"><span data-stu-id="a1a4d-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="a1a4d-110">Диалоговое окно предупреждение не всегда отображается и отображается соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="a1a4d-111">Если этот параметр имеет значение NULL, диалоговое окно предупреждения отображаться не будет.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="a1a4d-112">*хсаурцерегкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1a4d-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a4d-113">Корневой раздел реестра для копируемого параметра пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a4d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1a4d-114">Return value</span></span>



| <span data-ttu-id="a1a4d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a1a4d-115">Return code</span></span>                                                                          | <span data-ttu-id="a1a4d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a1a4d-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a1a4d-117"><dt>**УСЛОВИЯ**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a4d-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="a1a4d-118">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="a1a4d-119"><dt>**ISFALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="a1a4d-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="a1a4d-120">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a1a4d-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="a1a4d-121">Examples</span></span>

<span data-ttu-id="a1a4d-122">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="a1a4d-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="a1a4d-123">В следующем примере показано, как получить указатель на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="a1a4d-124">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="a1a4d-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="a1a4d-125">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="a1a4d-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="a1a4d-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a1a4d-126">Requirements</span></span>



| <span data-ttu-id="a1a4d-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a1a4d-127">Requirement</span></span> | <span data-ttu-id="a1a4d-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a1a4d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a4d-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1a4d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a4d-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1a4d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a1a4d-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1a4d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a4d-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1a4d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a1a4d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a1a4d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1a4d-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1a4d-134"><dt>Input.dll</dt></span></span> </dl> |



 

