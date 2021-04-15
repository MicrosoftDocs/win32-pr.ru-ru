---
description: Считывает указанный элемент данных из защищенного хранилища.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Метод Ипсторе:: ReadItem (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669136"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="68f3d-103">Метод Ипсторе:: ReadItem</span><span class="sxs-lookup"><span data-stu-id="68f3d-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="68f3d-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="68f3d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="68f3d-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="68f3d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="68f3d-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="68f3d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="68f3d-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="68f3d-108">Считывает указанный элемент данных из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="68f3d-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f3d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68f3d-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="68f3d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="68f3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f3d-111">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-112">Область хранилища поставщика.</span><span class="sxs-lookup"><span data-stu-id="68f3d-112">The provider storage area.</span></span>



| <span data-ttu-id="68f3d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="68f3d-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="68f3d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="68f3d-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="68f3d-115">PST-файл <dt>**\_ КЛЮЧ \_ текущего \_ пользователя**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="68f3d-116">Хранилище сохраняется в разделе реестра текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="68f3d-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="68f3d-117">PST-файл <dt>**\_ КЛЮЧ \_ Локальная \_ машина**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="68f3d-118">Хранилище сохраняется в разделе реестра локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="68f3d-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="68f3d-119">*питемтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-120">Указатель на идентификатор GUID, определяющий тип данных элемента для чтения.</span><span class="sxs-lookup"><span data-stu-id="68f3d-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="68f3d-121">*питемсубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-122">Указатель на идентификатор GUID, определяющий подтип данных элемента для чтения.</span><span class="sxs-lookup"><span data-stu-id="68f3d-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="68f3d-123">*сзитемнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-124">Указатель на строку, содержащую имя, присвоенное сохраненному элементу данных.</span><span class="sxs-lookup"><span data-stu-id="68f3d-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="68f3d-125">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-126">Значение **типа DWORD** , указывающее размер буфера, содержащего сохраненный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="68f3d-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="68f3d-127">*pbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-128">Указатель на буфер, содержащий сохраненный элемент данных.</span><span class="sxs-lookup"><span data-stu-id="68f3d-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="68f3d-129">*ппромптинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-130">Указатель на структуру [**PST \_ промптинфо**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="68f3d-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="68f3d-131">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68f3d-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3d-132">Указывает пользовательский интерфейс и поведение безопасности для операции чтения.</span><span class="sxs-lookup"><span data-stu-id="68f3d-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="68f3d-133">Значения флагов можно комбинировать с помощью логического или.</span><span class="sxs-lookup"><span data-stu-id="68f3d-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="68f3d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="68f3d-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="68f3d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="68f3d-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="68f3d-136">PST-файл <dt>**\_ Неограниченный \_ итемдата**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="68f3d-137">Указывает, что поток данных небезопасен.</span><span class="sxs-lookup"><span data-stu-id="68f3d-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="68f3d-138">По умолчанию вызовы элементов являются безопасными.</span><span class="sxs-lookup"><span data-stu-id="68f3d-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="68f3d-139">PST-файл <dt>**\_ \_Запрос**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="68f3d-140">Указывает, что подтверждение должно возвращаться после успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="68f3d-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="68f3d-141">Если пользовательский интерфейс включен, будет возвращено успешное выполнение **PST \_ E \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="68f3d-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="68f3d-142">Если пользовательский интерфейс не включен, возвращается значение **\_ \_ элемента \_ PST E** .</span><span class="sxs-lookup"><span data-stu-id="68f3d-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="68f3d-143">PST-файл <dt>**\_ БЕЗ \_ \_ миграции пользовательского интерфейса**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="68f3d-144">Не показывать пользовательский интерфейс, если не требуется специальный пароль.</span><span class="sxs-lookup"><span data-stu-id="68f3d-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f3d-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68f3d-145">Return value</span></span>

<span data-ttu-id="68f3d-146">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68f3d-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="68f3d-147">Значение **PST \_ E \_ OK** указывает, что функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="68f3d-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="68f3d-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68f3d-148">Remarks</span></span>

<span data-ttu-id="68f3d-149">Если **ReadItem** завершается успешно, приложение несет ответственность за освобождение возвращенного буфера данных с помощью функции [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .</span><span class="sxs-lookup"><span data-stu-id="68f3d-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f3d-150">Требования</span><span class="sxs-lookup"><span data-stu-id="68f3d-150">Requirements</span></span>



| <span data-ttu-id="68f3d-151">Требование</span><span class="sxs-lookup"><span data-stu-id="68f3d-151">Requirement</span></span> | <span data-ttu-id="68f3d-152">Значение</span><span class="sxs-lookup"><span data-stu-id="68f3d-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68f3d-153">Header</span><span class="sxs-lookup"><span data-stu-id="68f3d-153">Header</span></span><br/> | <dl> <span data-ttu-id="68f3d-154"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="68f3d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="68f3d-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="68f3d-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f3d-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f3d-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68f3d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f3d-158">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="68f3d-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="68f3d-159">**PST-файл \_ промптинфо**</span><span class="sxs-lookup"><span data-stu-id="68f3d-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
