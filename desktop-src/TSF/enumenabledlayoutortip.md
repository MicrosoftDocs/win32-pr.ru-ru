---
title: Функция Енуменабледлайаутортип
description: Перечисляет все включенные раскладки клавиатуры или текстовые службы указанного параметра пользователя.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Платформа текстовых служб Енуменабледлайаутортип Function
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681876"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="aaaba-104">Функция Енуменабледлайаутортип</span><span class="sxs-lookup"><span data-stu-id="aaaba-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="aaaba-105">Перечисляет все включенные раскладки клавиатуры или текстовые службы указанного параметра пользователя.</span><span class="sxs-lookup"><span data-stu-id="aaaba-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaaba-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aaaba-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="aaaba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="aaaba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaaba-108">*псзусеррег* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaba-109">Путь к реестру пользователя.</span><span class="sxs-lookup"><span data-stu-id="aaaba-109">The registry path of the user.</span></span> <span data-ttu-id="aaaba-110">Если этот параметр имеет **значение NULL**, \_ \_ используется текущий пользователь hKey.</span><span class="sxs-lookup"><span data-stu-id="aaaba-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="aaaba-111">*псзсистемрег* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaba-112">Путь реестра системы.</span><span class="sxs-lookup"><span data-stu-id="aaaba-112">The registry path of the system.</span></span> <span data-ttu-id="aaaba-113">Если этот параметр имеет **значение NULL**, \_ \_ используется система локального компьютера hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="aaaba-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="aaaba-114">*псзсофтваререг* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaba-115">Путь реестра программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="aaaba-115">The registry path of the software.</span></span> <span data-ttu-id="aaaba-116">Если этот параметр имеет **значение NULL**, \_ \_ \\ используется программное обеспечение для локального компьютера hKey.</span><span class="sxs-lookup"><span data-stu-id="aaaba-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="aaaba-117">*плайаутортиппрофиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaba-118">Указатель на буфер, который получает массив ЛАЙАУТОРТИППРОФИЛЕ.</span><span class="sxs-lookup"><span data-stu-id="aaaba-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="aaaba-119">*убуфленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaaba-120">Длина буфера, на который указывает *плайаутортиппрофиле*.</span><span class="sxs-lookup"><span data-stu-id="aaaba-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaaba-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aaaba-121">Return value</span></span>

<span data-ttu-id="aaaba-122">Если *плайаутортиппрофиле* имеет **значение NULL**, число элементов клавиатуры, включенных в параметре пользователя; в противном случае число элементов клавиатуры, копируемых в *плайаутортиппрофиле*.</span><span class="sxs-lookup"><span data-stu-id="aaaba-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="aaaba-123">Для языков редактора методов ввода (IME) возвращаются все редакторы IME, даже если включен только один редактор IME.</span><span class="sxs-lookup"><span data-stu-id="aaaba-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="aaaba-124">Например, если у пользователя включен новый быстрый редактор IME для CHT, функция **енуменабледлайаутортип** возвращает все 5 редакторов IME для CHT.</span><span class="sxs-lookup"><span data-stu-id="aaaba-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaaba-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aaaba-125">Remarks</span></span>

<span data-ttu-id="aaaba-126">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="aaaba-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="aaaba-127">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="aaaba-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="aaaba-128">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="aaaba-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="aaaba-129">Определение ЛАЙАУТОРТИППРОФИЛЕ:</span><span class="sxs-lookup"><span data-stu-id="aaaba-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="aaaba-130">Требования</span><span class="sxs-lookup"><span data-stu-id="aaaba-130">Requirements</span></span>



| <span data-ttu-id="aaaba-131">Требование</span><span class="sxs-lookup"><span data-stu-id="aaaba-131">Requirement</span></span> | <span data-ttu-id="aaaba-132">Значение</span><span class="sxs-lookup"><span data-stu-id="aaaba-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aaaba-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aaaba-133">Minimum supported client</span></span><br/> | <span data-ttu-id="aaaba-134">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aaaba-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aaaba-135">Minimum supported server</span></span><br/> | <span data-ttu-id="aaaba-136">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aaaba-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aaaba-137">DLL</span><span class="sxs-lookup"><span data-stu-id="aaaba-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaaba-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaaba-138"><dt>Input.dll</dt></span></span> </dl> |



 

