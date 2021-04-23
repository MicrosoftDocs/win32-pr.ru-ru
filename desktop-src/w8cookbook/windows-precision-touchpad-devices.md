---
title: Сенсорные устройства Windows Precision
description: Сенсорные устройства Windows Precision
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2020
ms.locfileid: "104412374"
---
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="37bdf-103">Сенсорные устройства Windows Precision</span><span class="sxs-lookup"><span data-stu-id="37bdf-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="37bdf-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="37bdf-104">Platforms</span></span>

<dl> <span data-ttu-id="37bdf-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="37bdf-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="37bdf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="37bdf-106">Description</span></span>

<span data-ttu-id="37bdf-107">Сенсорная панель Windows Precision — это новый класс входных устройств, обеспечивающих входные и жесты с высокой точностью.</span><span class="sxs-lookup"><span data-stu-id="37bdf-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="37bdf-108">По умолчанию эти устройства создают сообщения колесика прокрутки высокой точности для настольных приложений.</span><span class="sxs-lookup"><span data-stu-id="37bdf-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="37bdf-109">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="37bdf-109">Manifestations</span></span>

<span data-ttu-id="37bdf-110">Приложения, которые не предназначены для управления сообщениями с помощью колесика прокрутки с высокой точностью, могут прокручиваться или прокручиваться неправильно.</span><span class="sxs-lookup"><span data-stu-id="37bdf-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="37bdf-111">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="37bdf-111">Mitigation</span></span>

<span data-ttu-id="37bdf-112">Разработчикам приложений следует обратить внимание на сообщения с прокруткой при прокрутке с помощью колесика прокрутки мыши и соответствующим образом изменить их приложения. Однако в промежуточной версии приложения может не отказаться от перекрутки с высокой точностью на прокручивание (Дельта = 1) и выбрать получение сообщений с высоким уровнем точности с помощью колесика прокрутки (Дельта = 40) или стандартных сообщений с колесом прокрутки (Дельта = 120).</span><span class="sxs-lookup"><span data-stu-id="37bdf-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="37bdf-113">Решение</span><span class="sxs-lookup"><span data-stu-id="37bdf-113">Solution</span></span>

<span data-ttu-id="37bdf-114">Если приложение может обрабатывать сообщения с колесом прокрутки с высоким уровнем точности, ничего делать не нужно, так как это сообщение по умолчанию, отправляемое сенсорными окнами точности Windows.</span><span class="sxs-lookup"><span data-stu-id="37bdf-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="37bdf-115">Если приложение может обрабатывать сообщения с помощью колесика прокрутки с высокой точностью, но не сообщения с помощью колесика высокой точности, добавьте в манифест приложения следующее:</span><span class="sxs-lookup"><span data-stu-id="37bdf-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="37bdf-116">Если приложение не поддерживает обработку сообщений с помощью колесика прокрутки с высокой точностью или колесика высокой точности, добавьте следующий текст в манифест приложения, чтобы указать, что требуются стандартные сообщения колесика прокрутки:</span><span class="sxs-lookup"><span data-stu-id="37bdf-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




