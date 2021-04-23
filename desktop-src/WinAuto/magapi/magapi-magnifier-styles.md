---
title: Стили экранной лупы
description: В этом разделе описываются стили, используемые с элементом управления "Экранная лупа".
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415568"
---
# <a name="magnifier-styles"></a><span data-ttu-id="81f0e-103">Стили экранной лупы</span><span class="sxs-lookup"><span data-stu-id="81f0e-103">Magnifier Styles</span></span>

<span data-ttu-id="81f0e-104">В этом разделе описываются стили, используемые с элементом управления "Экранная лупа".</span><span class="sxs-lookup"><span data-stu-id="81f0e-104">This topic describes the styles used with the magnifier control.</span></span> <span data-ttu-id="81f0e-105">Чтобы создать элемент управления "Экранная лупа", используйте функцию [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) и укажите класс окна WC_MAGNIFIER, а также сочетание следующих стилей экранной лупы.</span><span class="sxs-lookup"><span data-stu-id="81f0e-105">To create a magnifier control, use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function and specify the WC_MAGNIFIER window class, along with a combination of the following magnifier styles.</span></span>

| <span data-ttu-id="81f0e-106">Требование</span><span class="sxs-lookup"><span data-stu-id="81f0e-106">Requirement</span></span> | <span data-ttu-id="81f0e-107">Значение</span><span class="sxs-lookup"><span data-stu-id="81f0e-107">Value</span></span> |
|:---|:---|
| <span data-ttu-id="81f0e-108">MS_CLIPAROUNDCURSOR 0x0002L</span><span class="sxs-lookup"><span data-stu-id="81f0e-108">MS_CLIPAROUNDCURSOR 0x0002L</span></span> | <span data-ttu-id="81f0e-109">Вырезает область окна экранной лупы, которая окружает системный курсор.</span><span class="sxs-lookup"><span data-stu-id="81f0e-109">Clips the area of the magnifier window that surrounds the system cursor.</span></span> <span data-ttu-id="81f0e-110">Этот стиль позволяет пользователю видеть содержимое экрана, которое находится за окном экранной лупы.</span><span class="sxs-lookup"><span data-stu-id="81f0e-110">This style enables the user to see screen content that is behind the magnifier window.</span></span> |
| <span data-ttu-id="81f0e-111">MS_INVERTCOLORS 0x0004L</span><span class="sxs-lookup"><span data-stu-id="81f0e-111">MS_INVERTCOLORS 0x0004L</span></span> | <span data-ttu-id="81f0e-112">Отображает увеличенное содержимое экрана с использованием инвертированных цветов.</span><span class="sxs-lookup"><span data-stu-id="81f0e-112">Displays the magnified screen content using inverted colors.</span></span> |
| <span data-ttu-id="81f0e-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span><span class="sxs-lookup"><span data-stu-id="81f0e-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span></span> | <span data-ttu-id="81f0e-114">Отображает увеличенный системный курсор вместе с увеличенным содержимым экрана.</span><span class="sxs-lookup"><span data-stu-id="81f0e-114">Displays the magnified system cursor along with the magnified screen content.</span></span> |

## <a name="requirements"></a><span data-ttu-id="81f0e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="81f0e-115">Requirements</span></span>

| <span data-ttu-id="81f0e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="81f0e-116">Requirement</span></span> | <span data-ttu-id="81f0e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="81f0e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="81f0e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81f0e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="81f0e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81f0e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="81f0e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81f0e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="81f0e-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81f0e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="81f0e-122">Header</span><span class="sxs-lookup"><span data-stu-id="81f0e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="81f0e-123"><dt>Увеличение. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f0e-123"><dt>Magnification.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="81f0e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81f0e-124">See also</span></span>

[<span data-ttu-id="81f0e-125">Константы</span><span class="sxs-lookup"><span data-stu-id="81f0e-125">Constants</span></span>](entry-magapi-constants.md)
