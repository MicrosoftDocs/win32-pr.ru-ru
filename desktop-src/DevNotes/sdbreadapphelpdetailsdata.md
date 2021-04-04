---
Description: Извлекает данные из базы данных сведений о AppHelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Функция Сдбреадапфелпдетаилсдата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988589"
---
# <a name="sdbreadapphelpdetailsdata-function"></a>Функция Сдбреадапфелпдетаилсдата

Извлекает данные из базы данных сведений о AppHelp.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Описатель для базы данных AppHelp Details, AppHelp. sdb.

</dd> <dt>

*pData* \[ заполняет\]
</dt> <dd>

Структура [**\_ данных APPHELP**](apphelp-data.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




