---
description: Определяет, поддерживает ли устройство ввода Мультисенсорная.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'Метод ITablet3:: Исмултитауч'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266149"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="c9a46-103">Метод ITablet3:: Исмултитауч</span><span class="sxs-lookup"><span data-stu-id="c9a46-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="c9a46-104">Определяет, поддерживает ли устройство ввода Мультисенсорная.</span><span class="sxs-lookup"><span data-stu-id="c9a46-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9a46-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="c9a46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9a46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a46-107">*бисмултитауч* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9a46-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a46-108">Указывает, является ли устройство Мультисенсорная.</span><span class="sxs-lookup"><span data-stu-id="c9a46-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a46-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9a46-109">Return value</span></span>

<span data-ttu-id="c9a46-110">Возвращает **\_ ОК** в случае успеха, в противном случае возвращает код ошибки, например **е \_ Failed**.</span><span class="sxs-lookup"><span data-stu-id="c9a46-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a46-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9a46-111">Remarks</span></span>

<span data-ttu-id="c9a46-112">После определения с помощью [**IRealTimeStylus3:: мултитаученаблед**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) или **ITablet3:: исмултитауч** , доступного для Мультисенсорная, приложение может выбрать для Мультисенсорная входных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c9a46-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="c9a46-113">Дополнительные сведения о методах фильтрации Мультисенсорная доступны в разделе Свойства **IRealTimeStylus3:: мултитаученаблед** .</span><span class="sxs-lookup"><span data-stu-id="c9a46-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="c9a46-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="c9a46-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="c9a46-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c9a46-115">Requirements</span></span>



| <span data-ttu-id="c9a46-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c9a46-116">Requirement</span></span> | <span data-ttu-id="c9a46-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c9a46-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a46-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9a46-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a46-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c9a46-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c9a46-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9a46-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a46-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9a46-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9a46-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9a46-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9a46-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9a46-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a46-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9a46-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a46-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="c9a46-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="c9a46-126">**мултитаученаблед**</span><span class="sxs-lookup"><span data-stu-id="c9a46-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




