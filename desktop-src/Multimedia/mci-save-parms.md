---
title: Структура MCI_SAVE_PARMS (МЦиапи. h)
description: '\_ \_ Структура пармс для сохранения данных содержит сведения о имени файла для \_ команды MCI Save.'
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- MCI_SAVE_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672531"
---
# <a name="mci_save_parms-structure"></a>\_Структура для сохранения пармс в MCI \_

Структура **\_ \_ пармс для сохранения** данных содержит сведения о имени файла для команды [**MCI \_ Save**](mci-save.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a>Члены

<dl> <dt>

**двкаллбакк**
</dt> <dd>

Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.

</dd> <dt>

**лпфиленаме**
</dt> <dd>

Имя сохраняемого файла.

</dd> </dl>

## <a name="remarks"></a>Комментарии

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

[**\_Сохранение MCI**](mci-save.md)
</dt> <dt>

[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

