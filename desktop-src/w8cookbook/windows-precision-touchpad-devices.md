---
title: устройства сенсорной панели Windows
description: устройства сенсорной панели Windows
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb81978c9c9849dfa0d073a4b37af3760d1d4e5bc8e8fa2e81317293db04fc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007904"
---
# <a name="windows-precision-touchpad-devices"></a>устройства сенсорной панели Windows

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8.1  
</dl>

## <a name="description"></a>Описание

сенсорная панель Windows Precision — это новый класс входных устройств, обеспечивающих входные и жесты с высокой точностью. По умолчанию эти устройства создают сообщения колесика прокрутки высокой точности для настольных приложений.

## <a name="manifestations"></a>Проявлениями

Приложения, которые не предназначены для управления сообщениями с помощью колесика прокрутки с высокой точностью, могут прокручиваться или прокручиваться неправильно.

## <a name="mitigation"></a>Меры по снижению риска

Разработчикам приложений следует обратить внимание на сообщения с прокруткой при прокрутке с помощью колесика прокрутки мыши и соответствующим образом изменить их приложения. Однако в промежуточной версии приложения может не отказаться от перекрутки с высокой точностью на прокручивание (Дельта = 1) и выбрать получение сообщений с высоким уровнем точности с помощью колесика прокрутки (Дельта = 40) или стандартных сообщений с колесом прокрутки (Дельта = 120).

## <a name="solution"></a>Решение

если приложение может обрабатывать сообщения с колесом прокрутки с высоким уровнем точности, ничего делать не нужно, так как это сообщение по умолчанию, отправленное сенсорными панелью Windowsной точности.

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



 

 




