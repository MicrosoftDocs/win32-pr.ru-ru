---
title: Функция Енумлайаутортипфорсетуп
description: Перечисляет установленные раскладки клавиатуры и текстовые службы для пользовательского интерфейса установки или OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Платформа текстовых служб Енумлайаутортипфорсетуп Function
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681856"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="e5f31-104">Функция Енумлайаутортипфорсетуп</span><span class="sxs-lookup"><span data-stu-id="e5f31-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="e5f31-105">Перечисляет установленные раскладки клавиатуры и текстовые службы для пользовательского интерфейса установки или OOBE.</span><span class="sxs-lookup"><span data-stu-id="e5f31-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5f31-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5f31-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e5f31-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5f31-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5f31-108">*LangID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5f31-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f31-109">Идентификатор языка элемента для перечисления.</span><span class="sxs-lookup"><span data-stu-id="e5f31-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="e5f31-110">*плайаутортип* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5f31-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f31-111">Указатель на буфер, который получает массив структур ЛАЙАУТОРТИП.</span><span class="sxs-lookup"><span data-stu-id="e5f31-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="e5f31-112">Может иметь **значение NULL** , чтобы получить количество элементов.</span><span class="sxs-lookup"><span data-stu-id="e5f31-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="e5f31-113">*убуфленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5f31-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f31-114">Длина буфера, на который указывает *плайаутортип*.</span><span class="sxs-lookup"><span data-stu-id="e5f31-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="e5f31-115">Это пропускается, если *плайаутортип* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e5f31-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e5f31-116">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5f31-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5f31-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e5f31-117">Not used.</span></span> <span data-ttu-id="e5f31-118">Это значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e5f31-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5f31-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5f31-119">Return value</span></span>

<span data-ttu-id="e5f31-120">Если *плайаутортип* имеет **значение NULL**, число элементов клавиатуры, зарегистрированных в системе; в противном случае число элементов клавиатуры, копируемых в *плайаутортип*.</span><span class="sxs-lookup"><span data-stu-id="e5f31-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5f31-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5f31-121">Remarks</span></span>

<span data-ttu-id="e5f31-122">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="e5f31-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="e5f31-123">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="e5f31-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="e5f31-124">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="e5f31-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="e5f31-125">Определение ЛАЙАУТОРТИП:</span><span class="sxs-lookup"><span data-stu-id="e5f31-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="e5f31-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e5f31-126">Requirements</span></span>



| <span data-ttu-id="e5f31-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e5f31-127">Requirement</span></span> | <span data-ttu-id="e5f31-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e5f31-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5f31-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5f31-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e5f31-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5f31-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5f31-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5f31-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e5f31-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5f31-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5f31-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e5f31-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5f31-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5f31-134"><dt>Input.dll</dt></span></span> </dl> |



 

