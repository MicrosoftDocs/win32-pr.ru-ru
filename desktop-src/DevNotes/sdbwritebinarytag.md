---
description: Записывает двоичные данные в указанную базу данных.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: Функция Сдбвритебинаритаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 06900cf49445b52c519b04f88ffc6d5b3ba539404bf64bd7f820a502f70ec2e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044854"
---
# <a name="sdbwritebinarytag-function"></a>Функция Сдбвритебинаритаг

Записывает двоичные данные в указанную базу данных.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pdb* \[ -файл окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости.

</dd> <dt>

*ттаг* \[ окне\]
</dt> <dd>

ТЕГ для записи. Этот тег должен иметь тип **\_ \_ binary типа Tag**.

</dd> <dt>

*pBuffer* \[ окне\]
</dt> <dd>

Буфер, содержащий данные. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*двсизе* \[ окне\]
</dt> <dd>

Размер буфера *pBuffer* в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбвритебинаритагфромфиле**](sdbwritebinarytagfromfile.md)
</dt> <dt>

[**сдбвритедвордтаг**](sdbwritedwordtag.md)
</dt> <dt>

[**сдбвритеквордтаг**](sdbwriteqwordtag.md)
</dt> <dt>

[**сдбвритестрингтаг**](sdbwritestringtag.md)
</dt> <dt>

[**сдбвритевордтаг**](sdbwritewordtag.md)
</dt> </dl>

 

 




