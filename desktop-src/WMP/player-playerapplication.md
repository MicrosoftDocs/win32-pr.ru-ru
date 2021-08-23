---
title: Player. Плайераппликатион
description: свойство плайераппликатион извлекает объект плайераппликатион при выполнении удаленного элемента управления проигрыватель Windows Media.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- проигрыватель Windows Media Player. плайераппликатион
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
ms.openlocfilehash: c47400fcba1cb1cd1679e747d4fdd49b155df921ec33a721f74df2ec25259600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995854"
---
# <a name="playerplayerapplication"></a>Player. Плайераппликатион

свойство **плайераппликатион** извлекает объект **плайераппликатион** при выполнении удаленного элемента управления проигрыватель Windows Media.

## <a name="syntax"></a>Синтаксис

**плайераппликатион**

## <a name="possible-values"></a>Возможные значения

Это свойство является объектом **плайераппликатион** , предназначенным только для чтения, или значением NULL.

## <a name="remarks"></a>Remarks

это свойство используется только при удаленном взаимодействии Windows Media плайерконтрол. если значение равно null, Windows Media плайерконтрол не внедряется в удаленном режиме.

Это свойство доступно только в коде C++ или в коде скрипта в обложек через глобальную переменную Плайераппликатион.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Глобальные атрибуты**](global-attributes.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Объект Плайераппликатион**](playerapplication-object.md)
</dt> <dt>

[**Реализация удаленного управления проигрывателем Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





