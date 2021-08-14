---
title: Метод Сетпрограмлист класса Win32_TSVirtualIP
description: Перезаписывает список программ, использующих виртуализацию IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпрограмлист
- Службы удаленных рабочих столов метода Сетпрограмлист, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетпрограмлист
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ac74ca1a718fe1ec3c561b70da935d00a15f1bcb040cb29464ed9b6e52195c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349610"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>Метод Сетпрограмлист \_ класса Win32 тсвиртуалип

Перезаписывает список программ, использующих виртуализацию IP.

## <a name="syntax"></a>Синтаксис


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Програмлист* \[ окне\]
</dt> <dd>

Тип: **строка \[ \]**

Массив строк, содержащий путь и имена файлов программ, использующих IP-виртуализацию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **unint32**

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсвиртуалип Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





