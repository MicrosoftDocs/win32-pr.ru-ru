---
description: Получает объект декодера, если он существует.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: Метод Енкодеддата. декодер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648948"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="14d70-103">Метод Енкодеддата. декодер</span><span class="sxs-lookup"><span data-stu-id="14d70-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="14d70-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="14d70-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="14d70-105">Вместо этого используйте [**класс асненкодеддата**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="14d70-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="14d70-106">Метод **декодера** получает объект декодера, если он существует.</span><span class="sxs-lookup"><span data-stu-id="14d70-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d70-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14d70-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="14d70-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14d70-108">Parameters</span></span>

<span data-ttu-id="14d70-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="14d70-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="14d70-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14d70-110">Remarks</span></span>

<span data-ttu-id="14d70-111">Если закодированные данные не имеют объекта декодера, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="14d70-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d70-112">Требования</span><span class="sxs-lookup"><span data-stu-id="14d70-112">Requirements</span></span>



| <span data-ttu-id="14d70-113">Требование</span><span class="sxs-lookup"><span data-stu-id="14d70-113">Requirement</span></span> | <span data-ttu-id="14d70-114">Значение</span><span class="sxs-lookup"><span data-stu-id="14d70-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14d70-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="14d70-115">End of client support</span></span><br/> | <span data-ttu-id="14d70-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14d70-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="14d70-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="14d70-117">End of server support</span></span><br/> | <span data-ttu-id="14d70-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14d70-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="14d70-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="14d70-119">Redistributable</span></span><br/>       | <span data-ttu-id="14d70-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="14d70-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14d70-121">DLL</span><span class="sxs-lookup"><span data-stu-id="14d70-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="14d70-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d70-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
