---
title: Сообщение TB_SAVERESTORE (Коммктрл. h)
description: Отправка этого сообщения для инициации сохранения или восстановления состояния панели инструментов.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Элементы управления Windows для TB_SAVERESTORE сообщений
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891410"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="841d6-104">\_Сообщение САВЕРЕСТОРЕ ТБ</span><span class="sxs-lookup"><span data-stu-id="841d6-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="841d6-105">Отправка этого сообщения для инициации сохранения или восстановления состояния панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="841d6-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="841d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="841d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="841d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="841d6-108">Флаг сохранения или восстановления.</span><span class="sxs-lookup"><span data-stu-id="841d6-108">Save or restore flag.</span></span> <span data-ttu-id="841d6-109">Если этот параметр имеет **значение true**, сведения сохраняются.</span><span class="sxs-lookup"><span data-stu-id="841d6-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="841d6-110">Если значение — **false**, данные восстанавливаются.</span><span class="sxs-lookup"><span data-stu-id="841d6-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="841d6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="841d6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="841d6-112">Указатель на структуру [**тбсавепарамс**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) , которая указывает раздел реестра, подраздел и имя значения для сведений о состоянии панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="841d6-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841d6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="841d6-113">Return value</span></span>

<span data-ttu-id="841d6-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="841d6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="841d6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="841d6-115">Remarks</span></span>

<span data-ttu-id="841d6-116">В версии 4,72 и более ранних, чтобы использовать это сообщение для сохранения или восстановления панели инструментов, родительское окно элемента управления ToolBar должно реализовать обработчик для кода уведомления [ТБН \_ жетбуттонинфо](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="841d6-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="841d6-117">Панель инструментов выдает это уведомление для получения сведений о каждой кнопке при ее восстановлении.</span><span class="sxs-lookup"><span data-stu-id="841d6-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="841d6-118">Версия 5,80 включает новый вариант сохранения и восстановления.</span><span class="sxs-lookup"><span data-stu-id="841d6-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="841d6-119">В начале процесса и при сохранении или восстановлении каждой кнопки приложение получит уведомление [ТБН \_ Save](tbn-save.md) или [ТБН \_ RESTORE](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="841d6-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="841d6-120">Чтобы использовать этот параметр, необходимо реализовать обработчики уведомлений, чтобы предоставить оболочке сведения о битовой карте и состоянии, необходимые для успешного сохранения или восстановления состояния панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="841d6-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="841d6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="841d6-121">Requirements</span></span>



| <span data-ttu-id="841d6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="841d6-122">Requirement</span></span> | <span data-ttu-id="841d6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="841d6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="841d6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="841d6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="841d6-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="841d6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="841d6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="841d6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="841d6-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="841d6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="841d6-128">Header</span><span class="sxs-lookup"><span data-stu-id="841d6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="841d6-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="841d6-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="841d6-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="841d6-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="841d6-131">**ТБ \_ САВЕРЕСТОРЕВ** (Юникод) и **ТБ \_ саверестореа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="841d6-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





