---
title: Структура MCI_SEEK_PARMS (МЦиапи. h)
description: '\_ \_ Структура ПАРМС поиска MCI содержит сведения о размещении для \_ команды MCI Seek.'
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- структура MCI_SEEK_PARMS Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 283e0a0f60b4eaf438943628b92bb33974823f6525526c5e5a6cb2e55acb6c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038254"
---
# <a name="mci_seek_parms-structure"></a>\_ \_ Структура ПАРМС поиска MCI

Структура **\_ \_ пармс поиска MCI** содержит сведения о размещении для команды [**MCI \_ Seek**](mci-seek.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**двто**
</dt> <dd>

Положение для поиска.

</dd> </dl>

## <a name="remarks"></a>Remarks

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**\_Поиск MCI**](mci-seek.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

