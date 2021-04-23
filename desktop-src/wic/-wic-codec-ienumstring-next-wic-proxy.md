---
description: 'Функция прокси компонента Windows Imaging Component (WIC) для Иенумстринг:: Next.'
ms.assetid: a3f6a32b-3043-4bea-a70b-0b4507b4e3a1
title: Функция IEnumString_Next_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Next_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ae3e25b355268fe63025692bf116b60b45122e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072717"
---
# <a name="ienumstring_next_wic_proxy-function"></a><span data-ttu-id="c901f-103">Иенумстринг \_ Следующая \_ \_ функция прокси-сервера WIC</span><span class="sxs-lookup"><span data-stu-id="c901f-103">IEnumString\_Next\_WIC\_Proxy function</span></span>

<span data-ttu-id="c901f-104">Функция прокси компонента Windows Imaging Component (WIC) для Иенумстринг:: Next.</span><span class="sxs-lookup"><span data-stu-id="c901f-104">Windows Imaging Component (WIC) proxy function for IEnumString::Next.</span></span>

## <a name="syntax"></a><span data-ttu-id="c901f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c901f-105">Syntax</span></span>


```C++
HRESULT IEnumString_Next_WIC_Proxy(
  _In_ IEnumString *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="c901f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c901f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c901f-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="c901f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c901f-108">Тип: \**иенумстринг \** _</span><span class="sxs-lookup"><span data-stu-id="c901f-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="c901f-109">парамдеск</span><span class="sxs-lookup"><span data-stu-id="c901f-109">PARAMDESC</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c901f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c901f-110">Return value</span></span>

<span data-ttu-id="c901f-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c901f-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c901f-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c901f-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c901f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c901f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c901f-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="c901f-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c901f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c901f-115">Requirements</span></span>



| <span data-ttu-id="c901f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c901f-116">Requirement</span></span> | <span data-ttu-id="c901f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c901f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c901f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c901f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c901f-119">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c901f-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c901f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c901f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c901f-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c901f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c901f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c901f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c901f-123"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c901f-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




