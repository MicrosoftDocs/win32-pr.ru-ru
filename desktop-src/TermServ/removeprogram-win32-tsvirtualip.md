---
title: Метод Ремовепрограм класса Win32_TSVirtualIP (Бдаифаце. h)
description: Удаляет программу из списка программ, использующих виртуализацию IP-адресов.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовепрограм
- Службы удаленных рабочих столов метода Ремовепрограм, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Ремовепрограм
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44d955c7547a308086ea365681a5991012fe65e390ebe296f031f0c0ef99856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058622"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a>Метод Ремовепрограм \_ класса Win32 тсвиртуалип

Удаляет программу из списка программ, использующих виртуализацию IP-адресов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Програмпас* \[ окне\]
</dt> <dd>

Тип: **строка**

Путь и имя файла программы, которую необходимо удалить из списка. Если программа не найдена, возвращается ошибка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Бдаифаце. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсвиртуалип Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





