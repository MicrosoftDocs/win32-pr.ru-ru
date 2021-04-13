---
title: Сообщение TB_HASACCELERATOR (Коммктрл. h)
description: Извлекает число кнопок панели инструментов с указанным символом ускорителя.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- Элементы управления Windows для TB_HASACCELERATOR сообщений
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490995"
---
# <a name="tb_hasaccelerator-message"></a><span data-ttu-id="0a5e8-104">\_Сообщение ХАСАКЦЕЛЕРАТОР ТБ</span><span class="sxs-lookup"><span data-stu-id="0a5e8-104">TB\_HASACCELERATOR message</span></span>

<span data-ttu-id="0a5e8-105">\[Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="0a5e8-106">Это сообщение может не поддерживаться в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a5e8-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="0a5e8-107">Извлекает число кнопок панели инструментов с указанным символом ускорителя.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-107">Retrieves a count of toolbar buttons that have the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a5e8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a5e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a5e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a5e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5e8-110">Значение типа **WCHAR** , представляющее входной символ ускорителя для проверки.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-110">A **WCHAR** representing the input accelerator character to test.</span></span>

</dd> <dt>

<span data-ttu-id="0a5e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a5e8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a5e8-112">Указатель **на целое число, которое** получает количество кнопок с символом ускорителя.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-112">Pointer to an **int** that receives the number of buttons that have the accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a5e8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a5e8-113">Return value</span></span>

<span data-ttu-id="0a5e8-114">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-114">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="0a5e8-115">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="0a5e8-115">Security Considerations</span></span>

<span data-ttu-id="0a5e8-116">Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-116">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a5e8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a5e8-117">Remarks</span></span>

<span data-ttu-id="0a5e8-118">Сначала система запрашивает все кнопки панели инструментов для соответствующих сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-118">First, the system queries all toolbar buttons for matching accelerators.</span></span> <span data-ttu-id="0a5e8-119">Если совпадений не найдено, система отправляет уведомление [ТБН \_ мапакцелератор](tbn-mapaccelerator.md) в родительское окно, запрашивая индекс кнопки с указанным символом ускорителя.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-119">If no matches are found, the system sends the [TBN\_MAPACCELERATOR](tbn-mapaccelerator.md) notification to the parent window, requesting the index of the button that has the specified accelerator character.</span></span> <span data-ttu-id="0a5e8-120">Если родительский объект предоставляет индекс, то счетчику присваивается значение 1.</span><span class="sxs-lookup"><span data-stu-id="0a5e8-120">If the parent provides an index, the count is set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5e8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0a5e8-121">Requirements</span></span>



| <span data-ttu-id="0a5e8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0a5e8-122">Requirement</span></span> | <span data-ttu-id="0a5e8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0a5e8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5e8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a5e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0a5e8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a5e8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a5e8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a5e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0a5e8-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a5e8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a5e8-128">Header</span><span class="sxs-lookup"><span data-stu-id="0a5e8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a5e8-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a5e8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





