---
title: Функция Мрмкреатеконфиг (Мрмресаурцеиндексер. h)
description: Создает новый инициализированный файл конфигурации PRI, определяющий заданные по умолчанию квалификаторы. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Меню функций Мрмкреатеконфиг и другие ресурсы
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661963"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="34706-105">Функция Мрмкреатеконфиг</span><span class="sxs-lookup"><span data-stu-id="34706-105">MrmCreateConfig function</span></span>

<span data-ttu-id="34706-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="34706-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="34706-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="34706-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="34706-108">Создает новый инициализированный файл конфигурации PRI, определяющий заданные по умолчанию квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="34706-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="34706-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="34706-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="34706-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34706-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="34706-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="34706-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34706-112">*платформверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34706-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34706-113">Тип: **[ **мрмплатформверсион**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="34706-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="34706-114">Версия платформы (*targetOsVersion*), используемая для создаваемого файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="34706-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="34706-115">*дефаулткуалифиерс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="34706-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="34706-116">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="34706-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="34706-117">Список квалификаторов ресурсов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34706-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="34706-118">Например, L "язык-EN-US \_ Scale-100 \_ контраст — Standard"</span><span class="sxs-lookup"><span data-stu-id="34706-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="34706-119">*аутпутксмлфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34706-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34706-120">Тип: **пквстр**</span><span class="sxs-lookup"><span data-stu-id="34706-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="34706-121">Путь к создаваемому файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="34706-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34706-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34706-122">Return value</span></span>

<span data-ttu-id="34706-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="34706-123">Type: **HRESULT**</span></span>

<span data-ttu-id="34706-124">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="34706-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="34706-125">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="34706-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="34706-126">Требования</span><span class="sxs-lookup"><span data-stu-id="34706-126">Requirements</span></span>



| <span data-ttu-id="34706-127">Требование</span><span class="sxs-lookup"><span data-stu-id="34706-127">Requirement</span></span> | <span data-ttu-id="34706-128">Значение</span><span class="sxs-lookup"><span data-stu-id="34706-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34706-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34706-129">Minimum supported client</span></span><br/> | <span data-ttu-id="34706-130">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="34706-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="34706-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34706-131">Minimum supported server</span></span><br/> | <span data-ttu-id="34706-132">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="34706-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="34706-133">Header</span><span class="sxs-lookup"><span data-stu-id="34706-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="34706-134"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="34706-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="34706-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34706-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="34706-136"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34706-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="34706-137">DLL</span><span class="sxs-lookup"><span data-stu-id="34706-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34706-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34706-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="34706-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34706-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34706-140">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="34706-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

