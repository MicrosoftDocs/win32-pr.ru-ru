---
title: UI_ALL_COMMANDS (Уириббон. h)
description: Задает константу, определяющую коллекцию команд, объявленных в файле ресурсов разметки.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710466"
---
# <a name="ui_all_commands"></a><span data-ttu-id="943f6-103">\_все \_ команды пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="943f6-103">UI\_ALL\_COMMANDS</span></span>

<span data-ttu-id="943f6-104">Задает константу, определяющую коллекцию команд, объявленных в файле ресурсов разметки.</span><span class="sxs-lookup"><span data-stu-id="943f6-104">Specifies a constant that identifies the collection of Commands declared in the Markup resource file.</span></span>

## <a name="remarks"></a><span data-ttu-id="943f6-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="943f6-105">Remarks</span></span>

<span data-ttu-id="943f6-106">**Пользовательский интерфейс \_ ВСЕ \_ команды** полезны, когда необходимо получить доступ к аналогичным свойствам во всех командах.</span><span class="sxs-lookup"><span data-stu-id="943f6-106">**UI\_ALL\_COMMANDS** is useful when it is necessary to access similar properties across all Commands.</span></span> <span data-ttu-id="943f6-107">Например, **Пользовательский интерфейс \_ все \_ команды** можно передать в [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) , чтобы сделать недействительными и обновить все команды ленты, запросив ведущее приложение о новых значениях свойств.</span><span class="sxs-lookup"><span data-stu-id="943f6-107">For example, **UI\_ALL\_COMMANDS** can be passed to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) to invalidate and refresh all Ribbon Commands by querying the host application for new property values.</span></span>

## <a name="requirements"></a><span data-ttu-id="943f6-108">Требования</span><span class="sxs-lookup"><span data-stu-id="943f6-108">Requirements</span></span>



| <span data-ttu-id="943f6-109">Требование</span><span class="sxs-lookup"><span data-stu-id="943f6-109">Requirement</span></span> | <span data-ttu-id="943f6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="943f6-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943f6-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="943f6-111">Minimum supported client</span></span><br/> | <span data-ttu-id="943f6-112">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы \[ только для настольных приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="943f6-112">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="943f6-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="943f6-113">Minimum supported server</span></span><br/> | <span data-ttu-id="943f6-114">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="943f6-114">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="943f6-115">Header</span><span class="sxs-lookup"><span data-stu-id="943f6-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="943f6-116"><dt>Уириббон. h</dt></span><span class="sxs-lookup"><span data-stu-id="943f6-116"><dt>Uiribbon.h</dt></span></span> </dl>                                             |
| <span data-ttu-id="943f6-117">IDL</span><span class="sxs-lookup"><span data-stu-id="943f6-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="943f6-118"><dt>Уириббон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="943f6-118"><dt>Uiribbon.idl</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="943f6-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="943f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943f6-120">Константы и перечисления</span><span class="sxs-lookup"><span data-stu-id="943f6-120">Constants and Enumerations</span></span>](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

