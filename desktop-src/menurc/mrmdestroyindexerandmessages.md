---
title: Функция Мрмдестройиндексерандмессажес (Мрмресаурцеиндексер. h)
description: Освобождает ресурсы компьютера, связанные с индексатором ресурсов.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Меню функций Мрмдестройиндексерандмессажес и другие ресурсы
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071997"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="89981-104">Функция Мрмдестройиндексерандмессажес</span><span class="sxs-lookup"><span data-stu-id="89981-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="89981-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="89981-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="89981-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="89981-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="89981-107">Освобождает ресурсы компьютера, связанные с индексатором ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89981-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="89981-108">Уничтожает обработчик, освобождает индексатор и удаляет все сообщения.</span><span class="sxs-lookup"><span data-stu-id="89981-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="89981-109">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="89981-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="89981-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89981-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="89981-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="89981-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89981-112">*индексатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89981-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89981-113">Тип: **[ **мрмресаурцеиндексерхандле**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="89981-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="89981-114">Маркер, идентифицирующий индексатор ресурсов, который необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="89981-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89981-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89981-115">Return value</span></span>

<span data-ttu-id="89981-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89981-116">Type: **HRESULT**</span></span>

<span data-ttu-id="89981-117">\_ОК, если функция прошла успешно, в противном случае — другое значение.</span><span class="sxs-lookup"><span data-stu-id="89981-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="89981-118">Чтобы определить успешность или сбой, используйте макросы Success () или FAILed () (определенные в файле Winerror. h).</span><span class="sxs-lookup"><span data-stu-id="89981-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="89981-119">Требования</span><span class="sxs-lookup"><span data-stu-id="89981-119">Requirements</span></span>



| <span data-ttu-id="89981-120">Требование</span><span class="sxs-lookup"><span data-stu-id="89981-120">Requirement</span></span> | <span data-ttu-id="89981-121">Значение</span><span class="sxs-lookup"><span data-stu-id="89981-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89981-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89981-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89981-123">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="89981-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="89981-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89981-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89981-125">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="89981-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="89981-126">Header</span><span class="sxs-lookup"><span data-stu-id="89981-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89981-127"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="89981-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="89981-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89981-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="89981-129"><dt>Мрмсуппорт. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89981-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="89981-130">DLL</span><span class="sxs-lookup"><span data-stu-id="89981-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89981-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89981-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="89981-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89981-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89981-133">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="89981-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

