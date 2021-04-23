---
description: Извлекает сведения, связанные с подтипом.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'Метод Ипсторе:: Жетсубтипеинфо (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: db7cb02d1c21b8bb1717514a6347339065e4f112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669018"
---
# <a name="ipstoregetsubtypeinfo-method"></a><span data-ttu-id="2fc97-103">Метод Ипсторе:: Жетсубтипеинфо</span><span class="sxs-lookup"><span data-stu-id="2fc97-103">IPStore::GetSubtypeInfo method</span></span>

<span data-ttu-id="2fc97-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2fc97-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2fc97-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="2fc97-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2fc97-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="2fc97-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2fc97-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="2fc97-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2fc97-108">Извлекает сведения, связанные с подтипом.</span><span class="sxs-lookup"><span data-stu-id="2fc97-108">Retrieves information associated with a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc97-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fc97-109">Syntax</span></span>


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2fc97-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fc97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc97-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fc97-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc97-112">Область хранилища поставщика.</span><span class="sxs-lookup"><span data-stu-id="2fc97-112">The provider storage area.</span></span>



| <span data-ttu-id="2fc97-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2fc97-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="2fc97-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2fc97-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="2fc97-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="2fc97-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="2fc97-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="2fc97-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="2fc97-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2fc97-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2fc97-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="2fc97-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2fc97-119">*птипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fc97-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc97-120">Указатель на идентификатор GUID, определяющий тип данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="2fc97-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="2fc97-121">*псубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fc97-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc97-122">Указатель на идентификатор GUID, определяющий подтип данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="2fc97-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="2fc97-123">*ппинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fc97-123">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc97-124">Указатель на структуру файла [**. \_ PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc97-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2fc97-125">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fc97-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc97-126">Reserved: значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2fc97-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc97-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fc97-127">Return value</span></span>

<span data-ttu-id="2fc97-128">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2fc97-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="2fc97-129">Значение PST \_ E \_ OK указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2fc97-129">A value of PST\_E\_OK indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc97-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2fc97-130">Requirements</span></span>



| <span data-ttu-id="2fc97-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2fc97-131">Requirement</span></span> | <span data-ttu-id="2fc97-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2fc97-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc97-133">Header</span><span class="sxs-lookup"><span data-stu-id="2fc97-133">Header</span></span><br/> | <dl> <span data-ttu-id="2fc97-134"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc97-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2fc97-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2fc97-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="2fc97-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fc97-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fc97-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fc97-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc97-138">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="2fc97-138">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="2fc97-139">**файл \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="2fc97-139">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
