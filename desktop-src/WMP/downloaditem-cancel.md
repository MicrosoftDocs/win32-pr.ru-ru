---
title: Довнлоадитем. Cancel, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Cancel отменяет скачивание.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- метод cancel проигрыватель Windows Media
- метод cancel проигрыватель Windows Media, класс довнлоадитем
- класс довнлоадитем проигрыватель Windows Media, метод cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6208719b5ac2e81fb9175db9de67bcf1f00ad7c34787ed1ab45251abd517bd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749735"
---
# <a name="downloaditemcancel-method"></a>Довнлоадитем. Cancel, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **Cancel** отменяет скачивание.

## <a name="syntax"></a>Синтаксис


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Отмененные элементы не удаляются из коллекции загрузки. Отмененные элементы возвращают **довнлоадстате** значение 4 (отменено).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Довнлоадитем**](downloaditem-object.md)
</dt> <dt>

[**Довнлоадитем. Довнлоадстате**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





