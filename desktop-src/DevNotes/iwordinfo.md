---
description: Интерфейс Ивординфо является компонентом языкового ресурса для японского языка. Объект анализирует текст и определяет отдельные слова, возвращая либо слова в строке, либо возвращает словарные (корневые) формы слов в тексте строки.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Интерфейс Ивординфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538384"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="a379a-104">Интерфейс Ивординфо</span><span class="sxs-lookup"><span data-stu-id="a379a-104">IWordInfo interface</span></span>

<span data-ttu-id="a379a-105">\[Этот интерфейс устарел и не поддерживается в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="a379a-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="a379a-106">Интерфейс **ивординфо** является компонентом языкового ресурса для японского языка.</span><span class="sxs-lookup"><span data-stu-id="a379a-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="a379a-107">Объект анализирует текст и определяет отдельные слова, возвращая либо слова в строке, либо возвращает словарные (корневые) формы слов в тексте строки.</span><span class="sxs-lookup"><span data-stu-id="a379a-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="a379a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a379a-108">Members</span></span>

<span data-ttu-id="a379a-109">Интерфейс **ивординфо** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a379a-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a379a-110">**Ивординфо** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a379a-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="a379a-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a379a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a379a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a379a-112">Methods</span></span>

<span data-ttu-id="a379a-113">Интерфейс **ивординфо** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a379a-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="a379a-114">Метод</span><span class="sxs-lookup"><span data-stu-id="a379a-114">Method</span></span>        | <span data-ttu-id="a379a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a379a-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a379a-116">**бреактекст**</span><span class="sxs-lookup"><span data-stu-id="a379a-116">**BreakText**</span></span> | <span data-ttu-id="a379a-117">Анализирует текст для поиска слов и предоставляет результаты для объекта [вордсинк](/previous-versions//ms691570(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a379a-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a379a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a379a-118">Remarks</span></span>

<span data-ttu-id="a379a-119">Этот интерфейс используется для получения японских разрывов слов или словарных форм для анализируемого текста.</span><span class="sxs-lookup"><span data-stu-id="a379a-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="a379a-120">Словарная форма слова — это унинфлектедая форма слова.</span><span class="sxs-lookup"><span data-stu-id="a379a-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="a379a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a379a-121">Requirements</span></span>



| <span data-ttu-id="a379a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a379a-122">Requirement</span></span> | <span data-ttu-id="a379a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a379a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a379a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a379a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a379a-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a379a-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a379a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a379a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a379a-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a379a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a379a-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a379a-128">End of client support</span></span><br/>    | <span data-ttu-id="a379a-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a379a-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="a379a-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a379a-130">End of server support</span></span><br/>    | <span data-ttu-id="a379a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a379a-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a379a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a379a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a379a-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a379a-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a379a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a379a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a379a-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="a379a-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="a379a-136">[вордсинк](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a379a-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
