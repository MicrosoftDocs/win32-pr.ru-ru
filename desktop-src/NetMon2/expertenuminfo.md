---
description: Структура ЕКСПЕРТЕНУМИНФО предоставляет сведения о эксперте.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Структура ЕКСПЕРТЕНУМИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662206"
---
# <a name="expertenuminfo-structure"></a>Структура ЕКСПЕРТЕНУМИНФО

Структура **експертенуминфо** предоставляет сведения о эксперте. Сетевой монитор выделяет память для структуры и передает ее эксперту при вызове функции [**регистрации экспертов**](register-expert.md) . Когда эксперт получает структуру, он должен заполнить всю информацию, сетевой монитор запросы.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**szName**
</dt> <dd>

Имя эксперта.

</dd> <dt>

**сзвендор**
</dt> <dd>

Имя поставщика, который создает эксперт.

</dd> <dt>

**сздескриптион**
</dt> <dd>

Описание эксперта. Значение элемента **сздескриптион** может быть **равно NULL**. Если имя слишком длинное, оно усекается в конфигурации средства просмотра по умолчанию.

</dd> <dt>

**Version**
</dt> <dd>

Значение должно быть равно нулю.

</dd> <dt>

**Флаги**
</dt> <dd>

Следующие флаги описывают эксперта.



| Значение                                                                                                                                                                                                                                                    | Значение                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**\_ \_ Настраиваемый флаг перечисления с \_ возможностью эксперта**</dt> </dl>                                          | Эксперт поддерживает вызовы метода [**Configure**](configure.md) . <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**\_средство просмотра флагов перечислений "Эксперт" \_ \_ \_ закрыто**</dt> </dl>                                   | Эксперту требуется частный (не общий) Просмотр событий. <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**\_флаг ПЕРЕЧИСЛЕНИЯ эксперта \_ \_ нет \_ средства просмотра**</dt> </dl>                                                  | Эксперт не отправляет уведомления о событиях. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**\_флаг ПЕРЕЧИСЛЕНИЯ эксперта \_ \_ Добавить \_ меня \_ в \_ РМК \_ в \_ сводке**</dt> </dl> | Когда фокус находится на панели сводки, эксперт отображается в контекстном меню. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**\_флаг ПЕРЕЧИСЛЕНИЯ эксперта \_ \_ Добавить \_ меня \_ в \_ РМК \_ \_ подробно**</dt> </dl>    | Когда фокус находится на панели подробностей, он отображается в контекстном меню. <br/>  |



 

</dd> <dt>

**хексперт**
</dt> <dd>

Обрабатывайте эксперта. Если для регистрации эксперта используется структура **експертенуминфо** , параметр игнорируется.

</dd> <dt>

**сздллнаме**
</dt> <dd>

Закрытый член; не используйте.

</dd> <dt>

**хмодуле**
</dt> <dd>

Закрытый член; не используйте.

</dd> <dt>

**прегистерпрок**
</dt> <dd>

Закрытый член; не используйте.

</dd> <dt>

**пконфигпрок**
</dt> <dd>

Закрытый член; не используйте.

</dd> <dt>

**прунпрок**
</dt> <dd>

Закрытый член; не используйте.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




