---
title: Сообщение EM_SETTARGETDEVICE (RichEdit. h)
description: Задает целевое устройство и толщину линии, используемые для \ 0034; что вы получаете \ 0034; (WYSIWYG) форматирование в элементе управления Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- Элементы управления Windows для EM_SETTARGETDEVICE сообщений
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136255"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="646a3-104">\_Сообщение СЕТТАРЖЕТДЕВИЦЕ EM</span><span class="sxs-lookup"><span data-stu-id="646a3-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="646a3-105">Задает целевое устройство и толщину линии, используемой для "что вы видите" (WYSIWYG) в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="646a3-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="646a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="646a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="646a3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="646a3-108">HDC для целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="646a3-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="646a3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="646a3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="646a3-110">Толщина линии, используемой для форматирования.</span><span class="sxs-lookup"><span data-stu-id="646a3-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="646a3-111">Return value</span></span>

<span data-ttu-id="646a3-112">Возвращаемое значение равно нулю, если операция завершается с ошибкой, или ненулевой, если она завершается успешно.</span><span class="sxs-lookup"><span data-stu-id="646a3-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="646a3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="646a3-113">Remarks</span></span>

<span data-ttu-id="646a3-114">Параметр HDC для принтера по умолчанию можно получить следующим образом.</span><span class="sxs-lookup"><span data-stu-id="646a3-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="646a3-115">Если значение *lParam* равно нулю, разрывы строк не создаются.</span><span class="sxs-lookup"><span data-stu-id="646a3-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="646a3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="646a3-116">Requirements</span></span>



| <span data-ttu-id="646a3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="646a3-117">Requirement</span></span> | <span data-ttu-id="646a3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="646a3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="646a3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="646a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="646a3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="646a3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="646a3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="646a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="646a3-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="646a3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="646a3-123">Header</span><span class="sxs-lookup"><span data-stu-id="646a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="646a3-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="646a3-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





