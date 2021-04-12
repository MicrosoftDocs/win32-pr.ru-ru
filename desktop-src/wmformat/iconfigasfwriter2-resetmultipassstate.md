---
title: IConfigAsfWriter2 Ресетмултипассстате, метод
description: Метод Ресетмултипассстате сбрасывает фильтр, когда этап кодирования предварительной обработки отменяется до его завершения.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Формат Windows Media, Ресетмултипассстате метод
- Ресетмултипассстате метод Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 Windows Media Format, метод Ресетмултипассстате
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413450"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>Метод IConfigAsfWriter2:: Ресетмултипассстате

Метод **ресетмултипассстате** сбрасывает фильтр, когда этап кодирования предварительной обработки отменяется до его завершения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                         | Описание                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                | Метод выполнен успешно.<br/>                  |
| <dl> <dt>**VFW \_ E \_ не \_ остановлен**</dt> </dl> | Фильтр не находится в остановленном состоянии.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод должен вызываться для сброса внутреннего состояния фильтра при отмене этапа кодирования предварительной обработки до того, как фильтр получил событие **\_ \_ завершения предварительной обработки** . Нет необходимости вызывать этот метод, если процесс кодирования предварительной обработки завершается без ошибок.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

