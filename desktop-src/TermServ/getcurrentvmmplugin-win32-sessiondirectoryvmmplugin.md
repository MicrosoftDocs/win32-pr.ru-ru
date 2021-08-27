---
title: Метод Жеткуррентвммплугин класса Win32_SessionDirectoryVMMPlugin
description: Возвращает подключаемый модуль наивысшего приоритета, который включен.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеткуррентвммплугин
- Службы удаленных рабочих столов метода Жеткуррентвммплугин, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Жеткуррентвммплугин
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc683275581aeb00c654a30e8c5aba7fd920f58248b480fc39caa96c885bb7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080114"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Метод Жеткуррентвммплугин \_ класса Win32 сессиондиректоривммплугин

Возвращает подключаемый модуль наивысшего приоритета, который включен.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*sName* \[ заполняет\]
</dt> <dd>

Имя подключаемого модуля.

</dd> <dt>

*спровидер* \[ заполняет\]
</dt> <dd>

Имя поставщика подключаемого модуля.

</dd> <dt>

*ссервицелокатион* \[ заполняет\]
</dt> <dd>

Расположение службы, с которой должен связаться подключаемый модуль.

</dd> <dt>

*склассид* \[ заполняет\]
</dt> <dd>

Идентификатор класса подключаемого модуля.

</dd> <dt>

*Приоритет* \[ заполняет\]
</dt> <dd>

Приоритет подключаемого модуля. Чем выше значение, тем выше приоритет подключаемого модуля.

</dd> <dt>

*Включено* \[ заполняет\]
</dt> <dd>

Указывает, включен ли или отключен подключаемый модуль. **Значение true** , если подключаемый модуль включен или **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Сессиондиректоривммплугин Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





