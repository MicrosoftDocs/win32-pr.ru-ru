---
title: Ивмпсеттингс baseURL, свойство
description: Свойство baseURL получает или задает базовый URL-адрес, используемый для разрешения относительных путей с помощью команд сценария URL-адреса, внедренных в мультимедийное содержимое.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- Проигрыватель Windows Media для свойства baseURL
- baseURL свойство проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717771"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="a940b-106">Свойство Ивмпсеттингс:: baseURL</span><span class="sxs-lookup"><span data-stu-id="a940b-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="a940b-107">Свойство **baseURL** получает или задает базовый URL-адрес, используемый для разрешения относительных путей с помощью команд сценария URL-адреса, внедренных в мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="a940b-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="a940b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a940b-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="a940b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a940b-109">Property value</span></span>

<span data-ttu-id="a940b-110">**Строка System. String** , которая является базовым URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="a940b-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a940b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a940b-111">Remarks</span></span>

<span data-ttu-id="a940b-112">Это свойство указывает базовый URL-адрес HTTP, который передается в качестве параметра команды для события **аксвиндовсмедиаплайер \_ вмпокксевентс \_ скрипткоммандевент** .</span><span class="sxs-lookup"><span data-stu-id="a940b-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="a940b-113">Базовый URL-адрес объединяется с относительным URL-адресом следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a940b-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="a940b-114">В значение, полученное с помощью свойства **baseURL** , добавляется Замыкающая косая черта (/).</span><span class="sxs-lookup"><span data-stu-id="a940b-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="a940b-115">Начальный период, обратная косая черта или символ косой черты (., \\ и/) удаляются из относительного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a940b-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="a940b-116">Относительный URL-адрес добавляется в конец базового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a940b-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="a940b-117">Все символы косой черты в результирующем полном URL-адресе указываются в том же направлении (преобразованном в прямую или обратную косую черту) в зависимости от направления первого символа косой черты, обнаруженного в новом URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="a940b-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="a940b-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a940b-118">**Note**</span></span>

<span data-ttu-id="a940b-119">Элемент управления проигрывателя Windows Media не поддерживает использование двух точек (..) в относительном URL-адресе для указания родителя текущего расположения.</span><span class="sxs-lookup"><span data-stu-id="a940b-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="a940b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a940b-120">Requirements</span></span>



| <span data-ttu-id="a940b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a940b-121">Requirement</span></span> | <span data-ttu-id="a940b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a940b-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a940b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="a940b-123">Version</span></span><br/>   | <span data-ttu-id="a940b-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a940b-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a940b-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a940b-125">Namespace</span></span><br/> | <span data-ttu-id="a940b-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a940b-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a940b-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="a940b-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a940b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a940b-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a940b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a940b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a940b-130">**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a940b-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="a940b-131">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a940b-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





