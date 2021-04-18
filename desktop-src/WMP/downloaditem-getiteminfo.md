---
title: Довнлоадитем. getItemInfo, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод getItemInfo извлекает значение атрибута для элемента загрузки.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод Windows Media Player, класс Довнлоадитем
- Класс Довнлоадитем Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694830"
---
# <a name="downloaditemgetiteminfo-method"></a>Довнлоадитем. getItemInfo, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **getItemInfo** извлекает значение атрибута для элемента загрузки.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ItemName* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута. Поддерживаемые значения: Албумартист, альбом, длительность, WM/provider, Title, Усерратинг и WM/Траккнумбер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку** , содержащую значение атрибута, заданного параметром *ItemName*.

## <a name="remarks"></a>Комментарии

Этот метод извлекает атрибуты, указанные с помощью строки описания BITS. См. раздел [соглашение о задании BITS в проигрывателе Windows Media](windows-media-player-bits-job-convention.md).

Этот метод поддерживается для фонового скачивания. Код не должен вызывать этот метод при использовании загрузки в режиме реального времени.

Этот метод может получать сведения о заданиях BITS, добавленных только в текущем сеансе проигрывателя Windows Media.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 10 или более поздней версии<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Довнлоадитем. тип**](downloaditem-type.md)
</dt> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> </dl>

 

 





