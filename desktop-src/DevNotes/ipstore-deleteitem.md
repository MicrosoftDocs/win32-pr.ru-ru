---
description: Удаляет указанный элемент из защищенного хранилища.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: 'Ипсторе: метод:D Елетеитем (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648934"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="d539d-103">Ипсторе: метод:D Елетеитем</span><span class="sxs-lookup"><span data-stu-id="d539d-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="d539d-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d539d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d539d-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="d539d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d539d-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="d539d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d539d-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d539d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d539d-108">Удаляет указанный элемент из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="d539d-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="d539d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d539d-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d539d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d539d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d539d-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d539d-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d539d-112">Область хранилища поставщика.</span><span class="sxs-lookup"><span data-stu-id="d539d-112">The provider storage area.</span></span>



| <span data-ttu-id="d539d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d539d-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="d539d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d539d-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="d539d-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d539d-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="d539d-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d539d-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="d539d-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d539d-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d539d-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d539d-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d539d-119">*питемтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d539d-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d539d-120">Указатель на **идентификатор GUID** , определяющий тип данных удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="d539d-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="d539d-121">*питемсубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d539d-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d539d-122">**Идентификатор GUID** , указывающий подтип элемента для удаления.</span><span class="sxs-lookup"><span data-stu-id="d539d-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="d539d-123">*сзитемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d539d-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d539d-124">Строка, содержащая имя удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="d539d-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="d539d-125">*ппромптинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d539d-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d539d-126">Указатель на структуру [**PST \_ промптинфо**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d539d-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d539d-127">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d539d-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d539d-128">Указывает пользовательский интерфейс и поведение безопасности для операции удаления.</span><span class="sxs-lookup"><span data-stu-id="d539d-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="d539d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d539d-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="d539d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d539d-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="d539d-131">PST-файл <dt>**\_ БЕЗ \_ \_ миграции пользовательского интерфейса**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d539d-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="d539d-132">Не показывать пользовательский интерфейс, если не требуется специальный пароль.</span><span class="sxs-lookup"><span data-stu-id="d539d-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d539d-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d539d-133">Return value</span></span>

<span data-ttu-id="d539d-134">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d539d-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="d539d-135">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d539d-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d539d-136">Требования</span><span class="sxs-lookup"><span data-stu-id="d539d-136">Requirements</span></span>



| <span data-ttu-id="d539d-137">Требование</span><span class="sxs-lookup"><span data-stu-id="d539d-137">Requirement</span></span> | <span data-ttu-id="d539d-138">Значение</span><span class="sxs-lookup"><span data-stu-id="d539d-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d539d-139">Header</span><span class="sxs-lookup"><span data-stu-id="d539d-139">Header</span></span><br/> | <dl> <span data-ttu-id="d539d-140"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d539d-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d539d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d539d-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="d539d-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d539d-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d539d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d539d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d539d-144">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="d539d-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="d539d-145">**PST-файл \_ промптинфо**</span><span class="sxs-lookup"><span data-stu-id="d539d-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
