---
description: Извлекает указатель интерфейса на поставщик хранилища.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Функция Псторекреатеинстанце (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: ce61a0d320b34ad09f4801d4ee5b53625e61501b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648803"
---
# <a name="pstorecreateinstance-function"></a><span data-ttu-id="fb71c-103">Функция Псторекреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="fb71c-103">PStoreCreateInstance function</span></span>

<span data-ttu-id="fb71c-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb71c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fb71c-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="fb71c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fb71c-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="fb71c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fb71c-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="fb71c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fb71c-108">\[Эта функция может быть изменена или недоступна в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="fb71c-108">\[This function may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="fb71c-109">Вместо этой функции используйте функции **CryptProtectData** и **CryptUnprotectData** .\]</span><span class="sxs-lookup"><span data-stu-id="fb71c-109">Use the **CryptProtectData** and **CryptUnprotectData** functions instead of this function.\]</span></span>

<span data-ttu-id="fb71c-110">Извлекает указатель интерфейса на поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb71c-110">Retrieves an interface pointer to a storage provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb71c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb71c-111">Syntax</span></span>


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fb71c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb71c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb71c-113">*пппровидер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fb71c-113">*ppProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb71c-114">Указатель на полученный указатель интерфейса для поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb71c-114">A pointer to the retrieved interface pointer for the storage provider.</span></span> <span data-ttu-id="fb71c-115">По завершении использования интерфейса уменьшите его число ссылок, вызвав метод [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="fb71c-115">When you finish using the interface, decrement its reference count by calling its [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="fb71c-116">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb71c-116">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb71c-117">*ппровидерид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb71c-117">*pProviderID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb71c-118">Указатель на **идентификатор GUID** , который идентифицирует поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb71c-118">A pointer to the **GUID** that identifies the storage provider.</span></span> <span data-ttu-id="fb71c-119">Если этот параметр имеет **значение NULL**, используется базовый поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb71c-119">If this parameter is **NULL**, then the base storage provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="fb71c-120">*сохраняется* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb71c-120">*pReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb71c-121">Процессу должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb71c-121">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb71c-122">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb71c-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb71c-123">Процессу должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="fb71c-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb71c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb71c-124">Return value</span></span>

<span data-ttu-id="fb71c-125">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fb71c-125">The return value is an **HRESULT**.</span></span> <span data-ttu-id="fb71c-126">Значение **S \_ ОК** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fb71c-126">A value of **S\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb71c-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb71c-127">Remarks</span></span>

<span data-ttu-id="fb71c-128">Эта функция не имеет связанной библиотеки импорта; его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fb71c-128">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb71c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="fb71c-129">Requirements</span></span>



| <span data-ttu-id="fb71c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="fb71c-130">Requirement</span></span> | <span data-ttu-id="fb71c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fb71c-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb71c-132">Header</span><span class="sxs-lookup"><span data-stu-id="fb71c-132">Header</span></span><br/> | <dl> <span data-ttu-id="fb71c-133"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb71c-133"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="fb71c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fb71c-134">DLL</span></span><br/>    | <dl> <span data-ttu-id="fb71c-135"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb71c-135"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb71c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb71c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb71c-137">**CryptProtectData**</span><span class="sxs-lookup"><span data-stu-id="fb71c-137">**CryptProtectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[<span data-ttu-id="fb71c-138">**CryptUnprotectData**</span><span class="sxs-lookup"><span data-stu-id="fb71c-138">**CryptUnprotectData**</span></span>](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
