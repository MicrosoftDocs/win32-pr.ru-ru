---
title: Ивмпсеттингс Инвокеурлс, свойство
description: Свойство Инвокеурлс получает или задает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Проигрыватель Windows Media для свойства Инвокеурлс
- Инвокеурлс свойство проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Инвокеурлс
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718176"
---
# <a name="iwmpsettingsinvokeurls-property"></a>Свойство Ивмпсеттингс:: Инвокеурлс

Свойство **инвокеурлс** получает или задает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение **System. Boolean** , указывающее, должны ли события URL запускаться в веб-браузере. Значение по умолчанию — **true**.

## <a name="remarks"></a>Комментарии

Цифровые файлы мультимедиа и потоки могут содержать команды сценария URL-адреса. При отправке команды скрипта URL-адреса элементу управления проигрывателя Windows Media он сначала передается обработчику событий **аксвиндовсмедиаплайер \_ вмпокксевентс \_ скрипткоммандевент** независимо от значения, полученного **инвокеурлс**. После выхода **\_ Вмпокксевентс \_ Скрипткоммандевент** проигрыватель Windows Media проверяет **инвокеурлс** , чтобы определить, следует ли запускать веб-браузер по умолчанию с URL-адресом. Вы можете выборочно отображать URL-адреса, проверив их в **\_ вмпокксевентс \_ скрипткоммандевент** и установив нужные **инвокеурлс** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





