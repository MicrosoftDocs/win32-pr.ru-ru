---
title: Сообщение LVM_GETEMPTYTEXT (Коммктрл. h)
description: Получает текст, предназначенный для отображения, когда элемент управления "список" отображается пустым. Отправьте это сообщение явным образом или с помощью \_ макроса Жетемптитекст ListView.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- Элементы управления Windows для LVM_GETEMPTYTEXT сообщений
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489060"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="0a3c3-105">\_Сообщение LVM жетемптитекст</span><span class="sxs-lookup"><span data-stu-id="0a3c3-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="0a3c3-106">Получает текст, предназначенный для отображения, когда элемент управления "список" отображается пустым.</span><span class="sxs-lookup"><span data-stu-id="0a3c3-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="0a3c3-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетемптитекст ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .</span><span class="sxs-lookup"><span data-stu-id="0a3c3-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a3c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a3c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a3c3-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a3c3-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a3c3-110">Размер буфера, на который указывает *lParam*, включая завершающее **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0a3c3-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0a3c3-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0a3c3-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a3c3-112">Указатель на заканчивающийся нулем буфер размером в Юникоде, заданный параметром *wParam* для получения текста.</span><span class="sxs-lookup"><span data-stu-id="0a3c3-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="0a3c3-113">Вызывающий объект отвечает за выделение буфера.</span><span class="sxs-lookup"><span data-stu-id="0a3c3-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a3c3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a3c3-114">Return value</span></span>

<span data-ttu-id="0a3c3-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0a3c3-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3c3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0a3c3-116">Requirements</span></span>



| <span data-ttu-id="0a3c3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0a3c3-117">Requirement</span></span> | <span data-ttu-id="0a3c3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0a3c3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3c3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a3c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a3c3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a3c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a3c3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a3c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a3c3-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a3c3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a3c3-123">Header</span><span class="sxs-lookup"><span data-stu-id="0a3c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a3c3-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a3c3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





