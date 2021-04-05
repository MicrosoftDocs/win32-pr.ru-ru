---
description: Содержит результаты запроса к базе данных оболочек для соответствующего исполняемого файла.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Структура СДБКУЕРИРЕСУЛТ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990469"
---
# <a name="sdbqueryresult-structure"></a>Структура СДБКУЕРИРЕСУЛТ

Содержит результаты запроса к базе данных оболочек для соответствующего исполняемого файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a>Члены

<dl> <dt>

**атрексес**
</dt> <dd>

Значения **тагреф** для соответствующих исполняемых файлов. Обратите внимание, что **SDB \_ Max \_ exe** определяется как 16.

</dd> <dt>

**адвексефлагс**
</dt> <dd>

Этот параметр может принимать одно или несколько следующих значений.

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

**атрлайерс**
</dt> <dd>

Значения **тагреф** соответствующих слоев. Обратите внимание, что **SDB \_ Max \_ слоев** определяется как 8.

</dd> <dt>

**двлайерфлагс**
</dt> <dd>

Этот параметр может принимать одно или несколько следующих значений.

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

**трапфелп**
</dt> <dd>

Значение **тагреф** сообщения AppHelp соответствующего исполняемого файла.

</dd> <dt>

**двексекаунт**
</dt> <dd>

Число элементов в **атрексес**.

</dd> <dt>

**двлайеркаунт**
</dt> <dd>

Число элементов в **атрлайерс**.

</dd> <dt>

**guidID**
</dt> <dd>

Идентификатор GUID последнего исполняемого файла.

</dd> <dt>

**dwFlags**
</dt> <dd>

Этот параметр может принимать одно или несколько следующих значений.

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

**двкустомсдбмап**
</dt> <dd>

Схема пользовательских баз данных оболочек совместимости. Соответствующие биты задаются, если **рггуиддб** является допустимым.

</dd> <dt>

**рггуиддб**
</dt> <dd>

Идентификаторы GUID баз данных оболочек совместимости. Обратите внимание, что **SDB \_ Max \_ сдбс** определяется как 16.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбжетматчинжексе**](sdbgetmatchingexe.md)
</dt> </dl>

 

 




