---
title: Ивмпсеттингс Инвокеурлс, свойство
description: Свойство Инвокеурлс получает или задает значение, указывающее, должны ли события URL-адреса запускать веб-браузер.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- проигрыватель Windows Media свойства инвокеурлс
- проигрыватель Windows Media свойства инвокеурлс, интерфейс ивмпсеттингс
- проигрыватель Windows Media интерфейса ивмпсеттингс, свойство инвокеурлс
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
ms.openlocfilehash: dba44af7e6ec700f9df810486acb57af24a14c9e5d4966fddbfe4b242d346a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053432"
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

## <a name="remarks"></a>Remarks

Цифровые файлы мультимедиа и потоки могут содержать команды сценария URL-адреса. при отправке команды скрипта URL-адреса элементу управления проигрыватель Windows Media он сначала передается обработчику событий **аксвиндовсмедиаплайер \_ вмпокксевентс \_ скрипткоммандевент** независимо от значения, полученного **инвокеурлс**. после выхода **\_ вмпокксевентс \_ скрипткоммандевент** проигрыватель Windows Media проверяет **инвокеурлс** , чтобы определить, следует ли запускать веб-браузер по умолчанию с URL-адресом. Вы можете выборочно отображать URL-адреса, проверив их в **\_ вмпокксевентс \_ скрипткоммандевент** и установив нужные **инвокеурлс** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





