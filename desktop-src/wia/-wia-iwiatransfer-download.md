---
description: Инициирует загрузку данных в вызывающий объект.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: 'Ивиатрансфер: метод:D гружать (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541967"
---
# <a name="iwiatransferdownload-method"></a><span data-ttu-id="b6354-103">Ивиатрансфер: метод:D гружать</span><span class="sxs-lookup"><span data-stu-id="b6354-103">IWiaTransfer::Download method</span></span>

<span data-ttu-id="b6354-104">Инициирует загрузку данных в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="b6354-104">Initiates a data download to the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6354-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6354-105">Syntax</span></span>


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="b6354-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6354-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6354-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6354-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6354-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="b6354-108">Type: **LONG**</span></span>

<span data-ttu-id="b6354-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="b6354-109">Currently unused.</span></span> <span data-ttu-id="b6354-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="b6354-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b6354-111">*пивиатрансферкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b6354-111">*pIWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6354-112">Тип: \**[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="b6354-112">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="b6354-113">Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* \*](-wia-iwiatransfercallback.md) вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="b6354-113">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6354-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6354-114">Return value</span></span>

<span data-ttu-id="b6354-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b6354-115">Type: **HRESULT**</span></span>

<span data-ttu-id="b6354-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b6354-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6354-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6354-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6354-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6354-118">Remarks</span></span>

<span data-ttu-id="b6354-119">При скачивании папки также переносятся все дочерние элементы этой папки.</span><span class="sxs-lookup"><span data-stu-id="b6354-119">If a folder is downloaded, then all the child items of that folder are also transferred.</span></span> <span data-ttu-id="b6354-120">Каждый элемент передается в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="b6354-120">Each item is transferred in a separate stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6354-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b6354-121">Requirements</span></span>



| <span data-ttu-id="b6354-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b6354-122">Requirement</span></span> | <span data-ttu-id="b6354-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b6354-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6354-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6354-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6354-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6354-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6354-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6354-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6354-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6354-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b6354-128">Header</span><span class="sxs-lookup"><span data-stu-id="b6354-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6354-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6354-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b6354-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b6354-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6354-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6354-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="b6354-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6354-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6354-133"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6354-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




