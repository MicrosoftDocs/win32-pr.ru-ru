---
description: Возвращает интерфейс для перечисления подтипов типов, зарегистрированных в настоящий момент в защищенной базе данных.
ms.assetid: 07cc43ce-2191-4b20-b23d-d96d15aa8dea
title: 'Метод Ипсторе:: Енумсубтипес (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumSubtypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f0e5aafbfdadebfa96254b3bd5997ec8d07cfb64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668964"
---
# <a name="ipstoreenumsubtypes-method"></a><span data-ttu-id="6091f-103">Метод Ипсторе:: Енумсубтипес</span><span class="sxs-lookup"><span data-stu-id="6091f-103">IPStore::EnumSubtypes method</span></span>

<span data-ttu-id="6091f-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6091f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6091f-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="6091f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6091f-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="6091f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6091f-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6091f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6091f-108">Возвращает интерфейс для перечисления подтипов типов, зарегистрированных в настоящий момент в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="6091f-108">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6091f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6091f-109">Syntax</span></span>


```C++
HRESULT EnumSubtypes(
  [in]       PST_KEY          Key,
  [in] const GUID             *pType,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="6091f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6091f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6091f-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6091f-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6091f-112">Указывает, является ли тип локальным для компьютера или связан только с созданием пользователя.</span><span class="sxs-lookup"><span data-stu-id="6091f-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="6091f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6091f-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="6091f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6091f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="6091f-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="6091f-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="6091f-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6091f-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="6091f-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6091f-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6091f-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6091f-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6091f-119">*птипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6091f-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6091f-120">Указатель на идентификатор GUID, определяющий тип данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="6091f-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="6091f-121">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6091f-121">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6091f-122">Reserved: значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6091f-122">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6091f-123">*ппенум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6091f-123">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6091f-124">Указатель на интерфейс [**иенумпсторетипес**](ienumpstoretypes.md) , используемый для перечисления подтипов.</span><span class="sxs-lookup"><span data-stu-id="6091f-124">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to enumerate the subtypes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6091f-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6091f-125">Return value</span></span>

<span data-ttu-id="6091f-126">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6091f-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="6091f-127">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6091f-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6091f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="6091f-128">Requirements</span></span>



| <span data-ttu-id="6091f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="6091f-129">Requirement</span></span> | <span data-ttu-id="6091f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="6091f-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6091f-131">Header</span><span class="sxs-lookup"><span data-stu-id="6091f-131">Header</span></span><br/> | <dl> <span data-ttu-id="6091f-132"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6091f-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6091f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6091f-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="6091f-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6091f-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6091f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6091f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6091f-136">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="6091f-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
