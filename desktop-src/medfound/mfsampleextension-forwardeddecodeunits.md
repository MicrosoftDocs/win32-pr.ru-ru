---
description: Возвращает объект типа Имфколлектион, содержащий объекты Имфсампле, которые содержат единицы уровня абстракции сети (Налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: Атрибут MFSampleExtension_ForwardedDecodeUnits (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719474"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="9b9db-103">Мфсампликстенсион \_ форвардеддекодеунитс, атрибут</span><span class="sxs-lookup"><span data-stu-id="9b9db-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="9b9db-104">Возвращает объект типа [**имфколлектион**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) , содержащий объекты [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , которые содержат единицы уровня абстракции сети (налус) и дополнительные модули сведений об улучшении (SEI), перенаправляемые декодером.</span><span class="sxs-lookup"><span data-stu-id="9b9db-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b9db-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9b9db-105">Data type</span></span>

<span data-ttu-id="9b9db-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="9b9db-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="9b9db-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b9db-107">Remarks</span></span>

<span data-ttu-id="9b9db-108">Коллекция содержит все пользовательские единицы налу/SEI, начиная с предыдущего кадра с удаленными байтами защиты эмуляции.</span><span class="sxs-lookup"><span data-stu-id="9b9db-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b9db-109">Требования</span><span class="sxs-lookup"><span data-stu-id="9b9db-109">Requirements</span></span>



| <span data-ttu-id="9b9db-110">Требование</span><span class="sxs-lookup"><span data-stu-id="9b9db-110">Requirement</span></span> | <span data-ttu-id="9b9db-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9b9db-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9db-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b9db-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9b9db-113">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="9b9db-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9b9db-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b9db-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9b9db-115">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="9b9db-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9b9db-116">Header</span><span class="sxs-lookup"><span data-stu-id="9b9db-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b9db-117"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b9db-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




