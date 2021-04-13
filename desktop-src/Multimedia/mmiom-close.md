---
title: Сообщение MMIOM_CLOSE (Ммсистем. h)
description: '\_Сообщение о закрытии ммиом отправляется в процедуру ввода-вывода функцией ммиоклосе, чтобы запросить закрытие файла.'
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535621"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="090da-104">\_Сообщение о закрытии ммиом</span><span class="sxs-lookup"><span data-stu-id="090da-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="090da-105">Сообщение **о \_ закрытии ммиом** отправляется в процедуру ввода-вывода функцией [**ммиоклосе**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , чтобы запросить закрытие файла.</span><span class="sxs-lookup"><span data-stu-id="090da-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="090da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="090da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090da-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*лклосефлагс*</span><span class="sxs-lookup"><span data-stu-id="090da-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="090da-108">Флаги, содержащиеся в параметре **вфлагс** объекта **ммиоклосе**.</span><span class="sxs-lookup"><span data-stu-id="090da-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090da-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="090da-109">Return Value</span></span>

<span data-ttu-id="090da-110">Возвращает нуль, если файл успешно закрыт, или ошибка в противном случае.</span><span class="sxs-lookup"><span data-stu-id="090da-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="090da-111">Требования</span><span class="sxs-lookup"><span data-stu-id="090da-111">Requirements</span></span>



| <span data-ttu-id="090da-112">Требование</span><span class="sxs-lookup"><span data-stu-id="090da-112">Requirement</span></span> | <span data-ttu-id="090da-113">Значение</span><span class="sxs-lookup"><span data-stu-id="090da-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090da-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="090da-114">Minimum supported client</span></span><br/> | <span data-ttu-id="090da-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="090da-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="090da-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="090da-116">Minimum supported server</span></span><br/> | <span data-ttu-id="090da-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="090da-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="090da-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="090da-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="090da-119"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="090da-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

