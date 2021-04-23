---
title: Функция Мрмкреатеконфигинмемори (Мрмресаурцеиндексер. h)
description: Создает новые инициализированные сведения о конфигурации PRI (как данные в памяти, а не в файле), определяющие указанные квалификаторы по умолчанию.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Меню функций Мрмкреатеконфигинмемори и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535081"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="e1029-104">Функция Мрмкреатеконфигинмемори</span><span class="sxs-lookup"><span data-stu-id="e1029-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="e1029-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e1029-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e1029-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e1029-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e1029-107">Создает новые инициализированные сведения о конфигурации PRI (как данные в памяти, а не в файле), определяющие указанные квалификаторы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1029-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="e1029-108">Функция выделяет память и возвращает указатель на эту память в *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="e1029-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="e1029-109">Вызовите [**мрмфримемори**](mrmfreememory.md) с тем же указателем, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="e1029-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="e1029-110">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e1029-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1029-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1029-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="e1029-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1029-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1029-113">*платформверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1029-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1029-114">Тип: **[ **мрмплатформверсион**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="e1029-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="e1029-115">Версия платформы (*targetOsVersion*), используемая для создания сведений о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e1029-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="e1029-116">*дефаулткуалифиерс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e1029-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1029-117">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="e1029-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="e1029-118">Список квалификаторов ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1029-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="e1029-119">Например, L "язык-EN-US \_ Scale-100 \_ контраст — Standard"</span><span class="sxs-lookup"><span data-stu-id="e1029-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="e1029-120">*аутпутксмлдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1029-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1029-121">Тип: **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="e1029-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="e1029-122">Адрес указателя на байт.</span><span class="sxs-lookup"><span data-stu-id="e1029-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="e1029-123">Функция выделяет память и возвращает указатель на эту память в *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="e1029-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="e1029-124">Вызовите [**мрмфримемори**](mrmfreememory.md) с помощью указателя на Byte, чтобы освободить эту память.</span><span class="sxs-lookup"><span data-stu-id="e1029-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="e1029-125">*аутпутксмлсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e1029-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1029-126">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="e1029-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="e1029-127">Адрес ULONG.</span><span class="sxs-lookup"><span data-stu-id="e1029-127">The address of a ULONG.</span></span> <span data-ttu-id="e1029-128">В _outputXmlSize \* функция возвращает размер выделенной памяти, на которую указывает *аутпутксмлдата*.</span><span class="sxs-lookup"><span data-stu-id="e1029-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1029-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1029-129">Return value</span></span>

<span data-ttu-id="e1029-130">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e1029-130">Type: **HRESULT**</span></span>

<span data-ttu-id="e1029-131">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="e1029-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="e1029-132">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="e1029-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1029-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e1029-133">Requirements</span></span>



| <span data-ttu-id="e1029-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e1029-134">Requirement</span></span> | <span data-ttu-id="e1029-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e1029-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1029-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1029-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e1029-137">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="e1029-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e1029-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1029-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e1029-139">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="e1029-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1029-140">Header</span><span class="sxs-lookup"><span data-stu-id="e1029-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1029-141"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1029-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="e1029-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1029-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1029-143"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1029-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="e1029-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e1029-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1029-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1029-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e1029-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1029-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1029-147">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="e1029-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

