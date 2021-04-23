---
title: Функция Мрмфримемори (Мрмресаурцеиндексер. h)
description: Освобождает память, выделенную Мрмкреатеконфигинмемори, Мрмкреатересаурцефилеинмемори, Мрмдумпприфилеинмемори и Мрмдумппридатаинмемори.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Меню функций Мрмфримемори и другие ресурсы
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661959"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="acd38-104">Функция Мрмфримемори</span><span class="sxs-lookup"><span data-stu-id="acd38-104">MrmFreeMemory function</span></span>

<span data-ttu-id="acd38-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="acd38-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="acd38-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="acd38-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="acd38-107">Освобождает память, выделенную [**мрмкреатеконфигинмемори**](mrmcreateconfiginmemory.md), [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md), [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md)и [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="acd38-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="acd38-108">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="acd38-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="acd38-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acd38-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="acd38-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="acd38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd38-111">*данные* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acd38-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acd38-112">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="acd38-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="acd38-113">Указатель на память, выделенную и возвращаемую [_ *мрмкреатеконфигинмемори* \*](mrmcreateconfiginmemory.md), [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md), [**мрмдумпприфилеинмемори**](mrmdumpprifileinmemory.md)или [**мрмдумппридатаинмемори**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="acd38-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd38-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acd38-114">Return value</span></span>

<span data-ttu-id="acd38-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acd38-115">Type: **HRESULT**</span></span>

<span data-ttu-id="acd38-116">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="acd38-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="acd38-117">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="acd38-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd38-118">Требования</span><span class="sxs-lookup"><span data-stu-id="acd38-118">Requirements</span></span>



| <span data-ttu-id="acd38-119">Требование</span><span class="sxs-lookup"><span data-stu-id="acd38-119">Requirement</span></span> | <span data-ttu-id="acd38-120">Значение</span><span class="sxs-lookup"><span data-stu-id="acd38-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acd38-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acd38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="acd38-122">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="acd38-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="acd38-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acd38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="acd38-124">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="acd38-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="acd38-125">Header</span><span class="sxs-lookup"><span data-stu-id="acd38-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="acd38-126"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="acd38-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="acd38-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="acd38-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="acd38-128"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acd38-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="acd38-129">DLL</span><span class="sxs-lookup"><span data-stu-id="acd38-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acd38-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acd38-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="acd38-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acd38-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd38-132">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="acd38-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

