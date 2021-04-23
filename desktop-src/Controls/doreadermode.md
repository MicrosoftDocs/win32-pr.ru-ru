---
title: Функция Дореадермоде
description: Включает режим чтения в окне.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Элементы управления Windows для функций Дореадермоде
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493353"
---
# <a name="doreadermode-function"></a><span data-ttu-id="ce49c-104">Функция Дореадермоде</span><span class="sxs-lookup"><span data-stu-id="ce49c-104">DoReaderMode function</span></span>

<span data-ttu-id="ce49c-105">\[**Дореадермоде** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="ce49c-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="ce49c-106">В последующих версиях он может быть недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="ce49c-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="ce49c-107">Включает режим чтения в окне.</span><span class="sxs-lookup"><span data-stu-id="ce49c-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce49c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce49c-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="ce49c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce49c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce49c-110">*прми* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce49c-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce49c-111">Тип: **преадермодеинфо**</span><span class="sxs-lookup"><span data-stu-id="ce49c-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="ce49c-112">Указатель на структуру [**реадермодеинфо**](readermodeinfo.md) , содержащую сведения об инициализации для режима чтения.</span><span class="sxs-lookup"><span data-stu-id="ce49c-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce49c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce49c-113">Return value</span></span>

<span data-ttu-id="ce49c-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ce49c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce49c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce49c-115">Remarks</span></span>

<span data-ttu-id="ce49c-116">Режим чтения активируется на поддерживаемых устройствах щелчком мыши, обычно с помощью третьей кнопки мыши или колесика прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ce49c-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="ce49c-117">Последующее перемещение мыши в заданной области прокручивает содержимое области, а не перемещает указатель.</span><span class="sxs-lookup"><span data-stu-id="ce49c-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="ce49c-118">За пределами этой области указатель мыши отображается и работает нормально.</span><span class="sxs-lookup"><span data-stu-id="ce49c-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="ce49c-119">Второе нажатие кнопки или колесика прокрутки освобождает устройство от режима чтения.</span><span class="sxs-lookup"><span data-stu-id="ce49c-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="ce49c-120">Эта функция не объявлена ни в одном общедоступном заголовке.</span><span class="sxs-lookup"><span data-stu-id="ce49c-120">This function is not declared in any public header.</span></span> <span data-ttu-id="ce49c-121">Чтобы использовать его, необходимо получить доступ к нему как с порядковым номером 383 из Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="ce49c-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce49c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ce49c-122">Requirements</span></span>



| <span data-ttu-id="ce49c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ce49c-123">Requirement</span></span> | <span data-ttu-id="ce49c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ce49c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce49c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce49c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ce49c-126">Windows Vista, \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce49c-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ce49c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce49c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ce49c-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce49c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ce49c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ce49c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce49c-130"><dt>Comctl32.dll (версия 4,72 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ce49c-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 





