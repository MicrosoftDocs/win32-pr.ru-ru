---
title: Сообщение MCIWNDM_NOTIFYMEDIA (VFW. h)
description: Сообщение МЦИВНДМ \_ нотифимедиа уведомляет родительское окно приложения о том, что носитель был изменен.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802014"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="d7851-104">\_Сообщение мЦивндм нотифимедиа</span><span class="sxs-lookup"><span data-stu-id="d7851-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="d7851-105">Сообщение **мЦивндм \_ нотифимедиа** уведомляет родительское окно приложения о том, что носитель был изменен.</span><span class="sxs-lookup"><span data-stu-id="d7851-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="d7851-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7851-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7851-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="d7851-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="d7851-108">Обработайте окно МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="d7851-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="d7851-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="d7851-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="d7851-110">Указатель на строку с завершающим нулем, содержащую новое имя файла.</span><span class="sxs-lookup"><span data-stu-id="d7851-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="d7851-111">Если носитель закрывается, он указывает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="d7851-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7851-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7851-112">Remarks</span></span>

<span data-ttu-id="d7851-113">Вы можете включить уведомления об изменениях мультимедиа, указав \_ стиль окна мЦивндф нотифимедиа.</span><span class="sxs-lookup"><span data-stu-id="d7851-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7851-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d7851-114">Requirements</span></span>



| <span data-ttu-id="d7851-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d7851-115">Requirement</span></span> | <span data-ttu-id="d7851-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d7851-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7851-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7851-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7851-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7851-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7851-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7851-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7851-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7851-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7851-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d7851-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7851-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7851-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 





