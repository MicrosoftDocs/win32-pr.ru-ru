---
description: Перенаправляет события указанного объекта Шеллфолдервиев в соответствующий обработчик событий Шеллфолдервиевок.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Шеллфолдервиевок. Сетфолдервиев, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985872"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="41896-103">Шеллфолдервиевок. Сетфолдервиев, метод</span><span class="sxs-lookup"><span data-stu-id="41896-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="41896-104">Перенаправляет события указанного объекта [**шеллфолдервиев**](shellfolderview.md) в соответствующий обработчик событий [**шеллфолдервиевок**](shellfolderviewoc-object.md) .</span><span class="sxs-lookup"><span data-stu-id="41896-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="41896-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41896-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="41896-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41896-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41896-107">*ошеллфолдервиев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41896-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41896-108">Тип: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="41896-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="41896-109">Объект [_ *шеллфолдервиев* \*](shellfolderview.md) .</span><span class="sxs-lookup"><span data-stu-id="41896-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="41896-110">Его события [**енумдоне**](shellfolderviewoc-enumdone.md) и [**SelectionChanged**](shellfolderview-selectionchanged.md) будут перенаправляться в соответствующий обработчик событий [**шеллфолдервиевок**](shellfolderviewoc-object.md) .</span><span class="sxs-lookup"><span data-stu-id="41896-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41896-111">Требования</span><span class="sxs-lookup"><span data-stu-id="41896-111">Requirements</span></span>



| <span data-ttu-id="41896-112">Требование</span><span class="sxs-lookup"><span data-stu-id="41896-112">Requirement</span></span> | <span data-ttu-id="41896-113">Значение</span><span class="sxs-lookup"><span data-stu-id="41896-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41896-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41896-114">Minimum supported client</span></span><br/> | <span data-ttu-id="41896-115">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="41896-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41896-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41896-116">Minimum supported server</span></span><br/> | <span data-ttu-id="41896-117">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41896-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="41896-118">Header</span><span class="sxs-lookup"><span data-stu-id="41896-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="41896-119"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="41896-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="41896-120">IDL</span><span class="sxs-lookup"><span data-stu-id="41896-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41896-121"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41896-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="41896-122">DLL</span><span class="sxs-lookup"><span data-stu-id="41896-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41896-123"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="41896-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
