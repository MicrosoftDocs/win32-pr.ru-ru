---
description: Дата и время создания отчета.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Локатиондисп. ДиспЦивикаддрессрепорт. timestamp, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b805454a6c2d62a58ba5a2a3de8f5b5095e1db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684452"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a><span data-ttu-id="54fee-103">Локатиондисп. ДиспЦивикаддрессрепорт. timestamp, свойство</span><span class="sxs-lookup"><span data-stu-id="54fee-103">LocationDisp.DispCivicAddressReport.Timestamp property</span></span>

<span data-ttu-id="54fee-104">\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="54fee-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="54fee-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="54fee-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="54fee-106">Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="54fee-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="54fee-107">Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="54fee-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="54fee-108">Дата и время создания отчета.</span><span class="sxs-lookup"><span data-stu-id="54fee-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="54fee-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="54fee-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fee-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54fee-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="54fee-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="54fee-111">Property value</span></span>

<span data-ttu-id="54fee-112">Это свойство является **датой** только для чтения.</span><span class="sxs-lookup"><span data-stu-id="54fee-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="54fee-113">Временные метки задаются в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="54fee-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="54fee-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54fee-114">Remarks</span></span>

<span data-ttu-id="54fee-115">Обратите внимание, что для языков сценариев, таких как Microsoft JScript, может потребоваться выполнить преобразование в другие форматы времени при отображении меток времени в виде строк.</span><span class="sxs-lookup"><span data-stu-id="54fee-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="54fee-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="54fee-116">Examples</span></span>

<span data-ttu-id="54fee-117">Пример использования этого свойства см. [в примере простого отчета об использовании административного адреса](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="54fee-117">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="54fee-118">Требования</span><span class="sxs-lookup"><span data-stu-id="54fee-118">Requirements</span></span>



| <span data-ttu-id="54fee-119">Требование</span><span class="sxs-lookup"><span data-stu-id="54fee-119">Requirement</span></span> | <span data-ttu-id="54fee-120">Значение</span><span class="sxs-lookup"><span data-stu-id="54fee-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="54fee-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54fee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54fee-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="54fee-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="54fee-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54fee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54fee-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="54fee-124">None supported</span></span><br/>                  |



 

