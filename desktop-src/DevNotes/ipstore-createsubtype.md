---
description: Создает указанный подтип в указанном типе.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Метод Ипсторе:: Креатесубтипе (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647998"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="0df8a-103">Метод Ипсторе:: Креатесубтипе</span><span class="sxs-lookup"><span data-stu-id="0df8a-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="0df8a-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0df8a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0df8a-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="0df8a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0df8a-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="0df8a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0df8a-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0df8a-108">Создает указанный подтип в указанном типе.</span><span class="sxs-lookup"><span data-stu-id="0df8a-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df8a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0df8a-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0df8a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0df8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df8a-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df8a-112">Указывает область хранилища поставщика.</span><span class="sxs-lookup"><span data-stu-id="0df8a-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="0df8a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0df8a-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="0df8a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0df8a-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="0df8a-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0df8a-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="0df8a-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="0df8a-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="0df8a-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0df8a-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0df8a-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="0df8a-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0df8a-119">*птипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df8a-120">Указатель на **идентификатор GUID** , определяющий тип данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="0df8a-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="0df8a-121">*псубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df8a-122">Указатель на **идентификатор GUID** , определяющий подтип данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="0df8a-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="0df8a-123">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df8a-124">Указатель на структуру файла [**. \_ PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0df8a-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0df8a-125">*прулес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df8a-126">Указатель на структуру [**PST \_ акцессрулесет**](pst-accessruleset.md) .</span><span class="sxs-lookup"><span data-stu-id="0df8a-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="0df8a-127">**Windows XP:** Этот параметр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="0df8a-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="0df8a-128">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df8a-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df8a-129">Процессу необходимо задать значение 0.</span><span class="sxs-lookup"><span data-stu-id="0df8a-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df8a-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0df8a-130">Return value</span></span>

<span data-ttu-id="0df8a-131">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0df8a-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="0df8a-132">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0df8a-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df8a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0df8a-133">Requirements</span></span>



| <span data-ttu-id="0df8a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0df8a-134">Requirement</span></span> | <span data-ttu-id="0df8a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0df8a-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0df8a-136">Header</span><span class="sxs-lookup"><span data-stu-id="0df8a-136">Header</span></span><br/> | <dl> <span data-ttu-id="0df8a-137"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df8a-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0df8a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0df8a-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="0df8a-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df8a-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df8a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0df8a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df8a-141">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="0df8a-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="0df8a-142">**PST-файл \_ акцессрулесет**</span><span class="sxs-lookup"><span data-stu-id="0df8a-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="0df8a-143">**файл \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="0df8a-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
