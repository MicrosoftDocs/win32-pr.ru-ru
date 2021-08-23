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
ms.openlocfilehash: a9e116080ffbfd81cff7dca8674b6be6fc977f3f7b3024bf32779887bde04d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404413"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




