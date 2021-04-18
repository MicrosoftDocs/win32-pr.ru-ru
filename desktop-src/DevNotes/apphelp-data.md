---
description: Содержит сведения о данных AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Структура APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655659"
---
# <a name="apphelp_data-structure"></a>\_Структура данных APPHELP

Содержит сведения о данных AppHelp.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**dwFlags**
</dt> <dd>

Этот параметр может иметь одно из следующих значений.

<dl> <dt>

<span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ оболочку совместимости** (0x00000001)
</dt> <dt>

<span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ APPHELP** (0x00000002)
</dt> <dt>

<span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Шимрег \_ APPHELP \_ NOUI)** (0x00000004)
</dt> <dt>

<span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Шимрег \_ APPHELP \_ Cancel** (0x10000000)
</dt> <dt>

<span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ SxS** (0x00000010)
</dt> <dt>

<span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ слой** (0x00000020)
</dt> <dt>

<span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ драйвер** (0x00000040)
</dt> </dl> </dd> <dt>

**двсеверити**
</dt> <dd>

Этот параметр может иметь значение "тип" \_ None (0).

</dd> <dt>

**двхтмлхелпид**
</dt> <dd>

Идентификатор HTML Help.

</dd> <dt>

**сзаппнаме**
</dt> <dd>

Имя приложения.

</dd> <dt>

**трексе**
</dt> <dd>

[**Тагреф**](tagref.md) соответствующего исполняемого файла.

</dd> <dt>

**сзурл**
</dt> <dd>

URL-адрес для ссылки AppHelp Online.

</dd> <dt>

**сзлинк**
</dt> <dd>

Текст ссылки для **сзурл**.

</dd> <dt>

**сзапптитле**
</dt> <dd>

Заголовок сообщения AppHelp.

</dd> <dt>

**сзконтакт**
</dt> <dd>

Контактные данные поставщика.

</dd> <dt>

**сздетаилс**
</dt> <dd>

Подробное сообщение AppHelp.

</dd> <dt>

**двдата**
</dt> <dd>

Определяемые пользователем данные, управляемые приложением.

</dd> <dt>

**бспентри**
</dt> <dd>

Этот член имеет **значение true** , если эта запись находится в базе данных пакета обновления, и **false** в противном случае.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбреадапфелпдетаилсдата**](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




