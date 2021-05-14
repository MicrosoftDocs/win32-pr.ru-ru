---
description: Отправляется расширением диспетчера файлов для получения типа окна диспетчера файлов, имеющего фокус ввода.
title: Сообщение FM_GETFOCUS (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841415"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="6576f-103">Сообщение FM- \_ фокуса</span><span class="sxs-lookup"><span data-stu-id="6576f-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="6576f-104">Отправляется расширением диспетчера файлов для получения типа окна диспетчера файлов, имеющего фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="6576f-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="6576f-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6576f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6576f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6576f-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6576f-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6576f-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6576f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6576f-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6576f-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6576f-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6576f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6576f-110">Return value</span></span>

<span data-ttu-id="6576f-111">Возвращает тип окна диспетчера файлов, имеющего фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="6576f-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="6576f-112">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="6576f-112">It can be one of the following values.</span></span>



| <span data-ttu-id="6576f-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6576f-113">Return code</span></span>                                                                                    | <span data-ttu-id="6576f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6576f-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="6576f-115"><dt>**ФМФОКУС \_ dir**</dt></span><span class="sxs-lookup"><span data-stu-id="6576f-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="6576f-116">Часть каталога в окне каталога.</span><span class="sxs-lookup"><span data-stu-id="6576f-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="6576f-117"><dt>**\_дерево фмфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="6576f-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="6576f-118">Древовидная часть окна каталога.</span><span class="sxs-lookup"><span data-stu-id="6576f-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="6576f-119"><dt>**\_диски фмфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="6576f-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="6576f-120">Панель диска в окне каталога.</span><span class="sxs-lookup"><span data-stu-id="6576f-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="6576f-121"><dt>**\_Поиск фмфокус**</dt></span><span class="sxs-lookup"><span data-stu-id="6576f-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="6576f-122">Окно результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="6576f-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="6576f-123">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="6576f-123">Requirements</span></span>



| <span data-ttu-id="6576f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6576f-124">Requirement</span></span> | <span data-ttu-id="6576f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6576f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6576f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6576f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6576f-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6576f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6576f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6576f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6576f-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6576f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6576f-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6576f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6576f-131"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="6576f-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




