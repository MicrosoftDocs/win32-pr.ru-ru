---
title: Функция обратного вызова Реадерскролл
description: Определяемая приложением функция обратного вызова, используемая при перемещении указателя мыши в область окна режима модуля чтения, объявленная в качестве активной области прокрутки.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Элементы управления Windows для функции обратного вызова Реадерскролл
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988592"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="d6821-104">Функция обратного вызова Реадерскролл</span><span class="sxs-lookup"><span data-stu-id="d6821-104">ReaderScroll callback function</span></span>

<span data-ttu-id="d6821-105">\[*Реадерскролл* доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d6821-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6821-106">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="d6821-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d6821-107">Определяемая приложением функция обратного вызова, используемая при перемещении указателя мыши в область окна режима модуля чтения, объявленная в качестве активной области прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d6821-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6821-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6821-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="d6821-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6821-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6821-110">*прми* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6821-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6821-111">Тип: **преадермодеинфо**</span><span class="sxs-lookup"><span data-stu-id="d6821-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="d6821-112">Указатель на структуру [**реадермодеинфо**](readermodeinfo.md) , которая была передана в функцию [**дореадермоде**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="d6821-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="d6821-113">Эта структура определяет окно режима модуля чтения и активную область прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d6821-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="d6821-114">*DX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d6821-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6821-115">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="d6821-115">Type: **int**</span></span>

<span data-ttu-id="d6821-116">Расстояние для горизонтальной прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d6821-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="d6821-117">Если в \_ структуре [**реадермодеинфо**](readermodeinfo.md) установлен флаг РМФ вертикалонли, это значение всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="d6821-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="d6821-118">*dy* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6821-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6821-119">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="d6821-119">Type: **int**</span></span>

<span data-ttu-id="d6821-120">Расстояние для вертикальной прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d6821-120">The distance to scroll vertically.</span></span> <span data-ttu-id="d6821-121">Если в \_ структуре [**реадермодеинфо**](readermodeinfo.md) установлен флаг РМФ хоризонталонли, это значение всегда равно 0.</span><span class="sxs-lookup"><span data-stu-id="d6821-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6821-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6821-122">Return value</span></span>

<span data-ttu-id="d6821-123">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d6821-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d6821-124">Эта функция всегда должна возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d6821-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6821-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6821-125">Remarks</span></span>

<span data-ttu-id="d6821-126">Когда приложение получает уведомление от этой функции, приложение несет ответственность за прокрутку окна режима чтения в направлении, указанном параметрами *DX* и *dy* .</span><span class="sxs-lookup"><span data-stu-id="d6821-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="d6821-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="d6821-127">Examples</span></span>

<span data-ttu-id="d6821-128">В следующем примере демонстрируется реализация этой функции с помощью пользовательской функции для выполнения прокрутки.</span><span class="sxs-lookup"><span data-stu-id="d6821-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="d6821-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d6821-129">Requirements</span></span>



| <span data-ttu-id="d6821-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d6821-130">Requirement</span></span> | <span data-ttu-id="d6821-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d6821-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d6821-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6821-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d6821-133">Windows Vista, \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6821-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6821-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6821-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d6821-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d6821-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

