---
description: Инициирует отправку данных одного элемента от вызывающего.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Метод Ивиатрансфер:: upload (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263131"
---
# <a name="iwiatransferupload-method"></a><span data-ttu-id="ff6b4-103">Метод Ивиатрансфер:: upload</span><span class="sxs-lookup"><span data-stu-id="ff6b4-103">IWiaTransfer::Upload method</span></span>

<span data-ttu-id="ff6b4-104">Инициирует отправку данных одного элемента от вызывающего.</span><span class="sxs-lookup"><span data-stu-id="ff6b4-104">Initiates a data upload of a single item from the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff6b4-105">Syntax</span></span>


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="ff6b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff6b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff6b4-107">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff6b4-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6b4-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="ff6b4-108">Type: **LONG**</span></span>

<span data-ttu-id="ff6b4-109">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="ff6b4-109">Currently unused.</span></span> <span data-ttu-id="ff6b4-110">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ff6b4-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ff6b4-111">*псаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff6b4-111">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6b4-112">Тип: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="ff6b4-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="ff6b4-113">Указывает указатель на данные [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="ff6b4-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) data.</span></span>

</dd> <dt>

<span data-ttu-id="ff6b4-114">_pIWiaTransferCallback \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ff6b4-114">_pIWiaTransferCallback\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6b4-115">Тип: \**[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="ff6b4-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="ff6b4-116">Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* \*](-wia-iwiatransfercallback.md) вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="ff6b4-116">Specifies a pointer to the caller's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff6b4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff6b4-117">Return value</span></span>

<span data-ttu-id="ff6b4-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff6b4-118">Type: **HRESULT**</span></span>

<span data-ttu-id="ff6b4-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ff6b4-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff6b4-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff6b4-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff6b4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ff6b4-121">Requirements</span></span>



| <span data-ttu-id="ff6b4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ff6b4-122">Requirement</span></span> | <span data-ttu-id="ff6b4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ff6b4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6b4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff6b4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ff6b4-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff6b4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ff6b4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff6b4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ff6b4-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff6b4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ff6b4-128">Header</span><span class="sxs-lookup"><span data-stu-id="ff6b4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff6b4-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff6b4-129"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="ff6b4-130">IDL</span><span class="sxs-lookup"><span data-stu-id="ff6b4-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff6b4-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff6b4-131"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="ff6b4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff6b4-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff6b4-133"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff6b4-133"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
