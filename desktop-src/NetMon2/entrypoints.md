---
description: Структура ENTRYPOINT определяет точки входа для функций экспорта, которые сетевой монитор используют для работы средства синтаксического анализа.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: Структура ENTRYPOINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990919"
---
# <a name="entrypoints-structure"></a>Структура ENTRYPOINT

Структура **EntryPoint** определяет точки входа для функций экспорта, которые сетевой монитор используют для работы средства синтаксического анализа.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Зарегистрировать**
</dt> <dd>

Указатель на реализацию функции [*регистрации экспертов*](register-expert.md) .

</dd> <dt>

**Отмена регистрации**
</dt> <dd>

Указатель на реализацию функции [**дерегистрации**](deregister.md) .

</dd> <dt>

**рекогнизефраме**
</dt> <dd>

Указатель на реализацию функции экспорта [**рекогнизефраме**](recognizeframe.md) .

</dd> <dt>

**аттачпропертиес**
</dt> <dd>

Указатель на реализацию функции экспорта [**аттачпропертиес**](attachproperties.md) .

</dd> <dt>

**форматпропертиес**
</dt> <dd>

Указатель на реализацию функции экспорта [**форматпропертиес**](formatproperties.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Функция **креатепротокол** использует структуру **EntryPoint** для предоставления указателей на сетевой монитор. Указатели должны быть указаны в порядке, указанном в разделе предыдущие элементы.

Функцию [**форматпропертиес**](formatproperties.md) не нужно реализовывать, если сетевой монитор не будет отображать данные протокола. Например, **форматпропертиес** не требуется реализовывать, если приложение экспорта использует выходные данные средства синтаксического анализа, а сетевой монитор не отображает выходные данные.



| Для получения информации о                                        | См.                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Какие анализаторы и как они работают с сетевой монитор. | [Анализаторы](parsers.md)                                  |
| Реализация функции **DllMain**  включает пример.        | [Реализация DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[аттачпропертиес](attachproperties.md)
</dt> <dt>

[креатепротокол](createprotocol.md)
</dt> <dt>

[Отмена регистрации](deregister.md)
</dt> <dt>

[форматпропертиес](formatproperties.md)
</dt> <dt>

[рекогнизефраме](recognizeframe.md)
</dt> <dt>

[Зарегистрировать](register-parser.md)
</dt> </dl>

 

 




