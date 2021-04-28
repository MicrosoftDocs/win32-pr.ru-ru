---
description: Шеллфолдервиев. Попупитеммену — создает контекстное меню для указанного элемента и возвращает выбранную командную строку.
title: Шеллфолдервиев. Попупитеммену, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083392"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="8372d-103">Шеллфолдервиев. Попупитеммену, метод</span><span class="sxs-lookup"><span data-stu-id="8372d-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="8372d-104">Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.</span><span class="sxs-lookup"><span data-stu-id="8372d-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8372d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8372d-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="8372d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8372d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8372d-107">*витем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8372d-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8372d-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8372d-108">Type: **Variant**</span></span>

<span data-ttu-id="8372d-109">Объект [**FolderItem**](folderitem.md) , для которого будет создано контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="8372d-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="8372d-110">*VX* \[ в, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="8372d-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8372d-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8372d-111">Type: **Variant**</span></span>

<span data-ttu-id="8372d-112">Горизонтальное расположение меню в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="8372d-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8372d-113">*Ви* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8372d-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8372d-114">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8372d-114">Type: **Variant**</span></span>

<span data-ttu-id="8372d-115">Вертикальное расположение меню в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="8372d-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8372d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8372d-116">Return value</span></span>

<span data-ttu-id="8372d-117">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="8372d-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="8372d-118">**Строка** , получающая командную строку.</span><span class="sxs-lookup"><span data-stu-id="8372d-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="8372d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8372d-119">Requirements</span></span>



| <span data-ttu-id="8372d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8372d-120">Requirement</span></span> | <span data-ttu-id="8372d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8372d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8372d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8372d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8372d-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8372d-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8372d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8372d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8372d-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8372d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8372d-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8372d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8372d-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8372d-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8372d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8372d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8372d-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8372d-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8372d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8372d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8372d-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="8372d-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
