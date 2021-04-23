---
description: Записывает элемент данных в защищенное хранилище.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Метод Ипсторе:: Вритеитем (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648952"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="a8078-103">Метод Ипсторе:: Вритеитем</span><span class="sxs-lookup"><span data-stu-id="a8078-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="a8078-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8078-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a8078-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="a8078-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a8078-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="a8078-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a8078-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a8078-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a8078-108">Записывает элемент данных в защищенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="a8078-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8078-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8078-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a8078-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8078-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8078-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-112">Область хранилища поставщика.</span><span class="sxs-lookup"><span data-stu-id="a8078-112">The provider storage area.</span></span>



| <span data-ttu-id="a8078-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="a8078-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="a8078-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="a8078-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8078-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="a8078-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="a8078-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="a8078-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a8078-119">*питемтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-120">Указатель на **идентификатор GUID** , определяющий тип данных записываемого элемента данных.</span><span class="sxs-lookup"><span data-stu-id="a8078-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="a8078-121">*питемсубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-122">Указатель на **идентификатор GUID** , определяющий подтип данных записываемого элемента данных.</span><span class="sxs-lookup"><span data-stu-id="a8078-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="a8078-123">*сзитемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-124">Указатель на строку, содержащую имя, присвоенное сохраненному элементу данных.</span><span class="sxs-lookup"><span data-stu-id="a8078-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="a8078-125">*cbData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a8078-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-126">Указатель на **DWORD** , указывающий размер буфера, содержащего сохраненный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="a8078-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="a8078-127">*ппбдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a8078-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-128">Указатель на буфер, содержащий записываемый элемент данных.</span><span class="sxs-lookup"><span data-stu-id="a8078-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="a8078-129">*ппрумптинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-130">Указатель на структуру [**PST \_ промптинфо**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a8078-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a8078-131">*двдефаултконфирматионстиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-132">Стиль подтверждения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8078-132">The default confirmation style.</span></span>



| <span data-ttu-id="a8078-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="a8078-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="a8078-135">PST-файл <dt>**\_ CF \_ по умолчанию**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="a8078-136">Позволяет пользователю выбрать стиль подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a8078-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="a8078-137">PST-файл <dt>**\_ CF \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="a8078-138">Принудительное создание автоматического элемента.</span><span class="sxs-lookup"><span data-stu-id="a8078-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="a8078-139">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8078-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8078-140">Пользовательский интерфейс и поведение системы безопасности для операции записи.</span><span class="sxs-lookup"><span data-stu-id="a8078-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="a8078-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="a8078-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="a8078-143">PST-файл <dt>**\_ БЕЗ \_ перезаписи**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="a8078-144">Указывает, что элемент должен быть создан в защищенном хранилище.</span><span class="sxs-lookup"><span data-stu-id="a8078-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="a8078-145">Перезапись существующего элемента запрещена.</span><span class="sxs-lookup"><span data-stu-id="a8078-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="a8078-146">PST-файл <dt>**\_ Неограниченный \_ итемдата**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="a8078-147">Указывает, что поток данных небезопасен.</span><span class="sxs-lookup"><span data-stu-id="a8078-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="a8078-148">По умолчанию вызовы элементов являются безопасными.</span><span class="sxs-lookup"><span data-stu-id="a8078-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8078-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8078-149">Return value</span></span>

<span data-ttu-id="a8078-150">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8078-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="a8078-151">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a8078-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8078-152">Требования</span><span class="sxs-lookup"><span data-stu-id="a8078-152">Requirements</span></span>



| <span data-ttu-id="a8078-153">Требование</span><span class="sxs-lookup"><span data-stu-id="a8078-153">Requirement</span></span> | <span data-ttu-id="a8078-154">Значение</span><span class="sxs-lookup"><span data-stu-id="a8078-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8078-155">Header</span><span class="sxs-lookup"><span data-stu-id="a8078-155">Header</span></span><br/> | <dl> <span data-ttu-id="a8078-156"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a8078-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a8078-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="a8078-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8078-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8078-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8078-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8078-160">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="a8078-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="a8078-161">**PST-файл \_ промптинфо**</span><span class="sxs-lookup"><span data-stu-id="a8078-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
