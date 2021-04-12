---
title: Структура MCI_GENERIC_PARMS (МЦиапи. h)
description: '\_Общая \_ Структура пармс MCI содержит маркер окна, принимающего сообщения уведомления. Эта структура используется для командных сообщений MCI с пустыми списками параметров.'
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490122"
---
# <a name="mci_generic_parms-structure"></a>\_Универсальная \_ Структура пармс MCI

**Общая структура \_ \_ пармс MCI** содержит маркер окна, принимающего сообщения уведомления. Эта структура используется для командных сообщений MCI с пустыми списками параметров.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Пармс и MCI **\_ закрывают \_** структуры **\_ \_ пармс** , идентичные структурам **\_ универсального \_ пармс MCI** .

При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>МЦиапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Структуры MCI**](mci-structures.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

