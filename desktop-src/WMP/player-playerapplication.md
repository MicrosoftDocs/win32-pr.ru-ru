---
title: Player. Плайераппликатион
description: Свойство Плайераппликатион извлекает объект Плайераппликатион при запуске удаленного элемента управления проигрывателя Windows Media.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Проигрыватель проигрывателя Windows Media Player. Плайераппликатион
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704406"
---
# <a name="playerplayerapplication"></a>Player. Плайераппликатион

Свойство **плайераппликатион** извлекает объект **плайераппликатион** при запуске удаленного элемента управления проигрывателя Windows Media.

## <a name="syntax"></a>Синтаксис

**плайераппликатион**

## <a name="possible-values"></a>Возможные значения

Это свойство является объектом **плайераппликатион** , предназначенным только для чтения, или значением NULL.

## <a name="remarks"></a>Комментарии

Это свойство используется только при удаленном взаимодействии с Windows Media Плайерконтрол. Если значение равно null, Плайерконтрол Windows Media не внедряется в удаленном режиме.

Это свойство доступно только в коде C++ или в коде скрипта в обложек через глобальную переменную Плайераппликатион.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Глобальные атрибуты**](global-attributes.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Объект Плайераппликатион**](playerapplication-object.md)
</dt> <dt>

[**Реализация удаленного управления проигрывателем Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





