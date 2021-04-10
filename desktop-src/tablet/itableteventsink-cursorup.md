---
description: Происходит, когда пользователь порождает перо из поверхности планшета дигитайзера.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Метод Итаблетевентсинк:: Курсоруп'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272632"
---
# <a name="itableteventsinkcursorup-method"></a><span data-ttu-id="36fb8-103">Метод Итаблетевентсинк:: Курсоруп</span><span class="sxs-lookup"><span data-stu-id="36fb8-103">ITabletEventSink::CursorUp method</span></span>

<span data-ttu-id="36fb8-104">Происходит, когда пользователь порождает перо из поверхности планшета дигитайзера.</span><span class="sxs-lookup"><span data-stu-id="36fb8-104">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="36fb8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36fb8-105">Syntax</span></span>


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a><span data-ttu-id="36fb8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36fb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36fb8-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36fb8-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36fb8-108">Идентификатор планшета.</span><span class="sxs-lookup"><span data-stu-id="36fb8-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="36fb8-109">*CID* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="36fb8-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36fb8-110">Идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="36fb8-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="36fb8-111">*нсериалнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36fb8-111">*nSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36fb8-112">Серийный номер пера.</span><span class="sxs-lookup"><span data-stu-id="36fb8-112">The serial number of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="36fb8-113">*кбпкт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36fb8-113">*cbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36fb8-114">Число байтов в пакете данных пера.</span><span class="sxs-lookup"><span data-stu-id="36fb8-114">The number of bytes in a stylus data packet.</span></span>

</dd> <dt>

<span data-ttu-id="36fb8-115">*пбпкт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36fb8-115">*pbPkt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36fb8-116">Данные пера, указывающие расположение, в котором перо было удалено из планшета.</span><span class="sxs-lookup"><span data-stu-id="36fb8-116">The stylus data indicating the location where the stylus was lifted from the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36fb8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36fb8-117">Return value</span></span>

<span data-ttu-id="36fb8-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="36fb8-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="36fb8-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36fb8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="36fb8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="36fb8-120">Requirements</span></span>



| <span data-ttu-id="36fb8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="36fb8-121">Requirement</span></span> | <span data-ttu-id="36fb8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="36fb8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36fb8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36fb8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="36fb8-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="36fb8-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36fb8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36fb8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="36fb8-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="36fb8-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="36fb8-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36fb8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="36fb8-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36fb8-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36fb8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36fb8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36fb8-130">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="36fb8-130">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




