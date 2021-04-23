---
description: Задает сведения о заданных параметрах.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Метод Ипсторе:: Сетпровпарам (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647954"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="5aaf9-103">Метод Ипсторе:: Сетпровпарам</span><span class="sxs-lookup"><span data-stu-id="5aaf9-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="5aaf9-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5aaf9-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5aaf9-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5aaf9-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="5aaf9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5aaf9-108">Задает сведения о заданных параметрах.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aaf9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aaf9-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5aaf9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aaf9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aaf9-111">*двпарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aaf9-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaf9-112">Содержит **\_ кэш PST \_ PP \_ flush \_ пароль** для очистки кэша паролей пользователей.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="5aaf9-113">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5aaf9-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaf9-114">Длина пароля в буфере.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5aaf9-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="5aaf9-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="5aaf9-116">Указатель на буфер, содержащий пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="5aaf9-117">Это значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5aaf9-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5aaf9-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5aaf9-119">Reserved: значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aaf9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5aaf9-120">Return value</span></span>

<span data-ttu-id="5aaf9-121">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5aaf9-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="5aaf9-122">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5aaf9-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aaf9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5aaf9-123">Requirements</span></span>



| <span data-ttu-id="5aaf9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5aaf9-124">Requirement</span></span> | <span data-ttu-id="5aaf9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5aaf9-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aaf9-126">Header</span><span class="sxs-lookup"><span data-stu-id="5aaf9-126">Header</span></span><br/> | <dl> <span data-ttu-id="5aaf9-127"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf9-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="5aaf9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5aaf9-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="5aaf9-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf9-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aaf9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5aaf9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aaf9-131">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="5aaf9-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
