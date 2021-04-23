---
description: Возвращает интерфейс для перечисления типов, которые в настоящее время зарегистрированы в защищенной базе данных.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: 'Метод Ипсторе:: Енумтипес (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73166a9fc1d76ae9f67528636eda567b9fa190a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647911"
---
# <a name="ipstoreenumtypes-method"></a><span data-ttu-id="277f0-103">Метод Ипсторе:: Енумтипес</span><span class="sxs-lookup"><span data-stu-id="277f0-103">IPStore::EnumTypes method</span></span>

<span data-ttu-id="277f0-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="277f0-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="277f0-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="277f0-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="277f0-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="277f0-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="277f0-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="277f0-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="277f0-108">Возвращает интерфейс для перечисления типов, которые в настоящее время зарегистрированы в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="277f0-108">Returns an interface for enumerating types that are currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="277f0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="277f0-109">Syntax</span></span>


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="277f0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="277f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277f0-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="277f0-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277f0-112">Указывает, является ли тип локальным для компьютера или связан только с созданием пользователя.</span><span class="sxs-lookup"><span data-stu-id="277f0-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="277f0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="277f0-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="277f0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="277f0-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="277f0-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="277f0-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="277f0-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="277f0-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="277f0-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="277f0-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="277f0-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="277f0-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="277f0-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="277f0-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277f0-120">Reserved: значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="277f0-120">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="277f0-121">*ппенум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="277f0-121">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277f0-122">Указатель на интерфейс [**иенумпсторетипес**](ienumpstoretypes.md) , который используется для выполнения задач перечисления.</span><span class="sxs-lookup"><span data-stu-id="277f0-122">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to perform the enumeration tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277f0-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="277f0-123">Return value</span></span>

<span data-ttu-id="277f0-124">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="277f0-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="277f0-125">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="277f0-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="277f0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="277f0-126">Requirements</span></span>



| <span data-ttu-id="277f0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="277f0-127">Requirement</span></span> | <span data-ttu-id="277f0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="277f0-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="277f0-129">Header</span><span class="sxs-lookup"><span data-stu-id="277f0-129">Header</span></span><br/> | <dl> <span data-ttu-id="277f0-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="277f0-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="277f0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="277f0-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="277f0-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="277f0-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277f0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="277f0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277f0-134">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="277f0-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
