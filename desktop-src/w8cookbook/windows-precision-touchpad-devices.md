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
# <a name="windows-precision-touchpad-devices"></a>Сенсорные устройства Windows Precision

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8.1  
</dl>

## <a name="description"></a>Описание

Сенсорная панель Windows Precision — это новый класс входных устройств, обеспечивающих входные и жесты с высокой точностью. По умолчанию эти устройства создают сообщения колесика прокрутки высокой точности для настольных приложений.

## <a name="manifestations"></a>Проявлениями

Приложения, которые не предназначены для управления сообщениями с помощью колесика прокрутки с высокой точностью, могут прокручиваться или прокручиваться неправильно.

## <a name="mitigation"></a>Меры по снижению риска

Разработчикам приложений следует обратить внимание на сообщения с прокруткой при прокрутке с помощью колесика прокрутки мыши и соответствующим образом изменить их приложения. Однако в промежуточной версии приложения может не отказаться от перекрутки с высокой точностью на прокручивание (Дельта = 1) и выбрать получение сообщений с высоким уровнем точности с помощью колесика прокрутки (Дельта = 40) или стандартных сообщений с колесом прокрутки (Дельта = 120).

## <a name="solution"></a>Решение

Если приложение может обрабатывать сообщения с колесом прокрутки с высоким уровнем точности, ничего делать не нужно, так как это сообщение по умолчанию, отправляемое сенсорными окнами точности Windows.

Если приложение может обрабатывать сообщения с помощью колесика прокрутки с высокой точностью, но не сообщения с помощью колесика высокой точности, добавьте в манифест приложения следующее:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Если приложение не поддерживает обработку сообщений с помощью колесика прокрутки с высокой точностью или колесика высокой точности, добавьте следующий текст в манифест приложения, чтобы указать, что требуются стандартные сообщения колесика прокрутки:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




